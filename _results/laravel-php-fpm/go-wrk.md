```bash
$ cd ./tools/go-wrk
$ go run go-wrk.go -M GET -c 20 -d 10 "http://localhost:100/api/time"  
```

**result:**
```
Running 10s test @ http://localhost:100/api/time
  20 goroutine(s) running concurrently
859 requests in 10.112938088s, 198.81KB read
Requests/sec:		84.94
Transfer/sec:		19.66KB
Avg Req Time:		235.458395ms
Fastest Request:	59.122172ms
Slowest Request:	342.49407ms
Number of Errors:	0
```
