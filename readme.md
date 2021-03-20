# Http_Server
HTTP Server for static HTML(in resources/index.html)  
Reactor model: The main thread responds to the request connection using EPOLL to know the fd changing, and the thread pool responds to the requests(read,write) to connections.
### Http_server Usage:
`g++ *.cpp -o http_server -pthread`  
`./http_server 10000(port)`    
### Webbench test
`cd test_presure/webbench-1.5`  
`make`  
`./webbench -c  10000(Number of links)  -t 5(second)  http://ip:port/index.html(URL)` 
### Example Exhibition  
(Changing document location in http_conn.cpp)
example:http://193.112.197.42:9999/index.html

### Update
**March 4th:** implemented resolution of the request header (GET method, host and port numbers, connection mode) and show a static html page  

### Project expansion direction  
* Clearing links without use for a long time    
* User registration and authentication:Upload used POST method  
* ...  
