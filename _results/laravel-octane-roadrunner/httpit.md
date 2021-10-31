```bash
$ cd ./tools/httpit
$ go run main.go --connections 20 --requests 1000 --duration 60s --method GET "http://localhost:100/api/time"
```

**result:**
```
Benchmarking http://localhost:100/api/time with 20 connections
█████████████████████████████████████████████████████████████ 100%
Requests:  10000/10000  Elapsed:  4.09s  Throughput:  771.18 KB/s
 Statistics        Avg              Stdev              Max        
  Reqs/sec       2464.30            460.06           3752.10      
  Latency         8.18ms            4.06ms           118.92ms     
HTTP codes:
  1xx - 0, 2xx - 10000, 3xx - 0, 4xx - 0, 5xx - 0
  Others - 0
 Done! 

```
