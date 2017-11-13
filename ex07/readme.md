# Multithreaded  Web Server

## Objectives
* 1.Learn a little bit about TCP and HTTP
* 2.Listen for TCP connections on a socket
* 3.Parse a tiny number of HTTP requests
* 4.Create a proper HTTP response
* 5.Simulating a Slow Request
* 6.Improve the throughput of our server with a thread pool
* 7.Graceful Shutdown and Cleanup

## TO DO
You should use your singlethreaded web server from ex05 like a base for your multithreaded web server.
A thread pool will allow you to process connections concurrently: you can start processing a new connection before an older connection is finished. This increases the throughput of server.

Here’s what you should implement: instead of waiting for each request to process before starting on the next one, you’ll send the processing of each connection to a different thread. The threads will come from a pool of four threads that spawns when program start. The reason why the number of threads should be limiting to a small number is that if you created a new thread for each request as the requests come in, someone making ten million requests to server could create havoc by using up all ofserver’s resources and grinding the processing of all requests to a halt.

Rather than spawning unlimited threads, you’ll have a fixed number of threads waiting in the pool. As requests come in, you’ll send the requests to the pool for processing. The pool will maintain a queue of incoming requests. Each of the threads in the pool will pop a request off of this queue, handle the request, and then ask the queue for another request. With this design, you can process N requests concurrently, where N is the number of threads. This still means that N long-running requests can cause requests to back up in the queue, but you should increased the number of long-running requests we can handle before that point from one to N.


