```bash
$ cd ./tools/go-wrk
$ go run go-wrk.go -M GET -c 20 -d 10 "http://localhost:100/api/time"  
```

**result:**
```
Running 10s test @ http://localhost:100/api/time
  20 goroutine(s) running concurrently
10031 requests in 10.000702219s, 1.96MB read
Requests/sec:		1003.03
Transfer/sec:		200.80KB
Avg Req Time:		19.939591ms
Fastest Request:	2.570292ms
Slowest Request:	506.890263ms
Number of Errors:	0
```
