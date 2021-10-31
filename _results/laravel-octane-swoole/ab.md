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


Server Software:        nginx
Server Hostname:        localhost
Server Port:            100

Document Path:          /api/time
Document Length:        Variable

Concurrency Level:      10
Time taken for tests:   0.504 seconds
Complete requests:      1000
Failed requests:        0
Total transferred:      217000 bytes
HTML transferred:       29000 bytes
Requests per second:    1982.19 [#/sec] (mean)
Time per request:       5.045 [ms] (mean)
Time per request:       0.504 [ms] (mean, across all concurrent requests)
Transfer rate:          420.05 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.1      0       0
Processing:     2    5   4.5      4     105
Waiting:        2    5   4.5      4     105
Total:          2    5   4.5      4     105

Percentage of the requests served within a certain time (ms)
  50%      4
  66%      5
  75%      5
  80%      5
  90%      7
  95%      8
  98%     10
  99%     12
 100%    105 (longest request)

```
