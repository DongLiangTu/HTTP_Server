# HTTP_Server
HTTP Server for static HTML(in resources/index.html)  
Reactor model: The main thread responds to the request connection using EPOLL to know the fd changing, and the thread pool responds to the requests(read,write) to connection.
### Http_server Usage:
`http_server 10000(port)`    
### Webbench test
`cd test_presure/webbench-1.5`  
`make`  
`./webbench -c  10000(Number of links)  -t 5(second)  http://169.254.205.163:port/index.html(URL)` 

