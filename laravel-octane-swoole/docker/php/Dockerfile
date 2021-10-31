FROM php:8.0-cli

ARG SWOOLE_VERSION='4.7.1'
ARG NODE_VERSION=14

WORKDIR /var/www

RUN apt-get update && apt-get install -y \
    zip \
    git \
    curl \
    wget \
    unzip \
    zlib1g-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    libfreetype6-dev \
    libxml2-dev \
    libzip-dev \
    libonig-dev \
    libcurl4-openssl-dev \
    pkg-config \
    libssl-dev \
    libpq-dev \
    libmagickwand-dev \
    ghostscript \
    && pecl install imagick redis xdebug \
    && docker-php-ext-enable imagick redis xdebug \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-configure zip \
    && docker-php-ext-configure pgsql \
    && docker-php-ext-install -j$(nproc) gd soap iconv pdo pdo_mysql pdo_pgsql pgsql zip mbstring exif pcntl \
    && docker-php-source delete

# install swoole
RUN cd /tmp \
    && wget "https://pecl.php.net/get/swoole-${SWOOLE_VERSION}.tgz" \
    && tar zxvf "swoole-${SWOOLE_VERSION}.tgz" \
    && cd "swoole-${SWOOLE_VERSION}" \
    && phpize \
    && ./configure  --enable-openssl \
    && make \
    && make install

# enable swoole
RUN touch /usr/local/etc/php/conf.d/swoole.ini \
    && echo 'extension=swoole.so' > /usr/local/etc/php/conf.d/swoole.ini

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

USER www

CMD ["/usr/local/bin/php", "/var/www/artisan", "octane:start", "--server=swoole", "--host=0.0.0.0", "--port=9000", "--max-requests=1000", "--workers=10"]
