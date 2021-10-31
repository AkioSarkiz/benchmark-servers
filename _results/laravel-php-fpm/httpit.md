```bash
$ cd ./tools/httpit
$ go run main.go --connections 20 --requests 1000 --duration 60s --method GET "http://localhost:100/api/time"
```

**result:**
```
Benchmarking http://localhost:100/api/time with 20 connections
█████████████████████████████████████████████████████████████ 100%
Requests:  10000/10000  Elapsed:  10.26s  Throughput:  326.03 KB/s
 Statistics        Avg              Stdev              Max        
  Reqs/sec       2340.17            727.44           3323.30      
  Latency        20.53ms           65.08ms           447.85ms     
HTTP codes:
  1xx - 0, 2xx - 10000, 3xx - 0, 4xx - 0, 5xx - 0
  Others - 0
 Done! 

```
