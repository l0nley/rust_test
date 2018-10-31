# rust_test

root@6f0e73735d82:/home/some# wrk -t12 -c400 -d30s http://localhost:5000/api/values
Running 30s test @ http://localhost:5000/api/values
  12 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    47.63ms   28.44ms 566.82ms   94.69%
    Req/Sec   724.09    175.48     2.59k    82.34%
  252860 requests in 30.10s, 42.92MB read
Requests/sec:   8401.21
Transfer/sec:      1.43MB

root@6f0e73735d82:/home/some# wrk -t12 -c400 -d30s http://localhost:1337/api/json
Running 30s test @ http://localhost:1337/api/json
  12 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    94.42ms  269.77ms   2.00s    90.89%
    Req/Sec     2.30k     2.21k    9.84k    49.95%
  776363 requests in 30.10s, 89.59MB read
  Socket errors: connect 0, read 0, write 0, timeout 2807
Requests/sec:  25793.25
Transfer/sec:      2.98MB

2 cpu docker container on my notebook.
