```bash
$ cd ./tools/go-wrk
$ go run go-wrk.go -M GET -c 20 -d 10 "http://localhost:100/api/time"  
```

**result:**
```
Running 10s test @ http://localhost:100/api/time
  20 goroutine(s) running concurrently
13129 requests in 10.001567896s, 2.82MB read
Requests/sec:		1312.69
Transfer/sec:		288.43KB
Avg Req Time:		15.235841ms
Fastest Request:	3.78581ms
Slowest Request:	136.276554ms
Number of Errors:	0
```
