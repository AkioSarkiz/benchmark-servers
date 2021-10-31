```bash
$ ab -l -n 1000 -c 10 http://localhost:100/api/time
```

**result:**
```

This is ApacheBench, Version 2.3 <$Revision: 1879490 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking localhost (be patient)
Completed 100 requests
Completed 200 requests
Completed 300 requests
Completed 400 requests
Completed 500 requests
Completed 600 requests
Completed 700 requests
Completed 800 requests
Completed 900 requests
Completed 1000 requests
Finished 1000 requests


Server Software:        nginx/1.21.1
Server Hostname:        localhost
Server Port:            100

Document Path:          /api/time
Document Length:        Variable

Concurrency Level:      10
Time taken for tests:   12.868 seconds
Complete requests:      1000
Failed requests:        0
Total transferred:      287000 bytes
HTML transferred:       29000 bytes
Requests per second:    77.71 [#/sec] (mean)
Time per request:       128.676 [ms] (mean)
Time per request:       12.868 [ms] (mean, across all concurrent requests)
Transfer rate:          21.78 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.0      0       0
Processing:    57  128  30.6    117     292
Waiting:       57  128  30.6    117     292
Total:         57  128  30.6    117     292

Percentage of the requests served within a certain time (ms)
  50%    117
  66%    118
  75%    119
  80%    120
  90%    155
  95%    198
  98%    278
  99%    283
 100%    292 (longest request)


```
