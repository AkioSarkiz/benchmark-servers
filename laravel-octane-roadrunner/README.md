# Run

```bash
docker-compose up -d
docker-compose exec php composer i
docker-compose exec php ./vendor/bin/rr get-binary
docker-compose exec php chmod +x ./rr
docker-compose down
docker-compose up -d
```
