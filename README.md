# helloWorld

"Hello World!" in 1000 different coding languages/web frameworks..

So far..

1. .Net Core 1.0 RC1/2
2. Rust with Iron


## brenchmarks..

### .NET CORE 1.0
wrk --latency -t12 -c100 -d10s http://localhost:5000/  
Running 10s test @ http://localhost:5000/
  12 threads and 100 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     1.27ms    0.85ms  44.62ms   96.70%
    Req/Sec     6.56k   699.26    16.27k    90.95%
  Latency Distribution
     50%    1.20ms
     75%    1.29ms
     90%    1.43ms
     99%    3.45ms
  786166 requests in 10.10s, 92.22MB read
Requests/sec:  77845.04
Transfer/sec:      9.13MB

### Rust & Iron
wrk --latency -t12 -c100 -d10s http://localhost:5000/  
Running 10s test @ http://localhost:5000/
  12 threads and 100 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     4.51ms  778.64us  93.57ms   94.39%
    Req/Sec     1.19k   482.40     1.91k    61.08%
  Latency Distribution
     50%    4.36ms
     75%    4.52ms
     90%    4.98ms
     99%    6.33ms
  142079 requests in 10.02s, 15.45MB read
Requests/sec:  14182.06
Transfer/sec:      1.54MB
