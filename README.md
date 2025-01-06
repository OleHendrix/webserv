# Webserv  

Webserv is a project written in C++ that implements a simple HTTP server, designed to handle client requests and serve responses in compliance with the HTTP/1.1 protocol. This project serves as an introduction to web server development, focusing on networking, HTTP request parsing, response generation, and concurrency.

## How It Works  

1. **HTTP Server Basics**  
   - The server listens for client connections on a specified port.  
   - It accepts and processes incoming HTTP requests (e.g., `GET`, `POST`, `DELETE`).  
   - It generates appropriate HTTP responses based on the request and serves files from a specified directory or virtual host.  

2. **Request Parsing**  
   - Requests are parsed to extract essential information such as the HTTP method, headers, and body.  
   - Supports handling of chunked transfer encoding and query strings.  

3. **Response Generation**  
   - The server generates responses with appropriate status codes (`200 OK`, `404 Not Found`, `500 Internal Server Error`, etc.).  
   - Serves static files (e.g., HTML, CSS, images) and supports directory listing.  

4. **Concurrency**  
   - The server handles multiple clients simultaneously using non-blocking sockets and multiplexing with `select` or `poll`.  

5. **Configuration**  
   - The server is configured using a `.conf` file that specifies settings such as:  
     - Server ports.  
     - Root directory.  
     - Error pages.  
     - Supported methods.  
     - CGI (Common Gateway Interface) execution.  

6. **CGI Support**  
   - The server executes CGI scripts (e.g., Python or PHP scripts) to dynamically generate content.  

7. **Error Handling**  
   - Implements robust error handling for invalid requests, inaccessible files, and server misconfigurations.  
   - Custom error pages are supported for a better user experience.  

## What I Learned  
- How HTTP/1.1 works, including request/response lifecycle and headers.  
- Parsing and handling HTTP requests and generating appropriate responses.  
- Using system calls like `socket`, `bind`, `listen`, and `accept` to manage network connections.  
- Implementing concurrency using non-blocking I/O and multiplexing with `select` or `poll`.  
- Configuring and executing CGI scripts for dynamic content generation.  
- Debugging and optimizing networked applications for reliability and performance.  
