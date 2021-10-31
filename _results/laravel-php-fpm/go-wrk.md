```bash
$ cd ./tools/go-wrk
$ go run go-wrk.go -M GET -c 20 -d 10 "http://localhost:100/api/time"  
```

**result:**
```
Running 10s test @ http://localhost:100/api/time
  20 goroutine(s) running concurrently
806 requests in 10.110975045s, 186.54KB read
Requests/sec:		79.72
Transfer/sec:		18.45KB
Avg Req Time:		250.892681ms
Fastest Request:	64.825689ms
Slowest Request:	525.883911ms
Number of Errors:	0
```
