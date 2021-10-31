```bash
$ cd ./tools/httpit
$ go run main.go --connections 20 --requests 1000 --duration 60s --method GET "http://localhost:100/api/time"
```

**result:**
```
Benchmarking http://localhost:100/api/time with 20 connections
█████████████████████████████████████████████████████████████ 100%
Requests:  10000/10000  Elapsed:  60.00s  Throughput:  30.61 KB/s
 Statistics        Avg              Stdev              Max        
  Reqs/sec        93.04             52.14             381.53      
  Latency        239.36ms          17.41ms           579.04ms     
HTTP codes:
  1xx - 0, 2xx - 10000, 3xx - 0, 4xx - 0, 5xx - 0
  Others - 0
 Done! 

```
