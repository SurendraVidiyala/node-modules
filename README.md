# node-modules
#Node modules: 
- HTTP, fs and path. At the end of this exercise, you will be able to:
- Implement a simple HTTP Server
- Implement a server that returns html files from a folder 
* A Simple HTTP Server
  - Create a folder named node-http at a convenient location and move into the folder.
  - In the node-http folder, create a subfolder named public.
- Create a file named server-1.js and add the following code to it:

````
var http = require('http');

var hostname = 'localhost';
var port = 3000;

var server = http.createServer(function(req, res){
  console.log(req.headers);
    res.writeHead(200, { 'Content-Type': 'text/html' });
  res.end('<html><body><h1>Hello World</h1></body></html>');
  })
server.listen(port, hostname, function(){
  console.log(`Server running at http://${hostname}:${port}/`);
});
````

