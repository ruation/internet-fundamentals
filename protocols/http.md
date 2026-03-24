# Hypertext Transfer Protocol (HTTP)

Whenever you go to a site with a URL that use HTTP, e.g. "http://www.github.com/", your browser turn this into a request message and sends it to the HTTP server. The HTTP server interprets the request message, and returns you an appropriate response message, which is either the resource you requested or an error message. This process is illustrated bellow:

- User issues a URL from a browser, e.g. "http://www.github.com/"
- Browser sends a request message, e.g. "GET URL HTTP/1:1"
- Server maps the URL to a file or program under the document directory. 
- Server returns a response message, e.g. "HTTP/1.1 200 OK"
- Browser formats the response and displays

## Uniform Resource Locator (URL)

**Syntax:**

protocol://hostname:port/path-and-file-name

- Protocol: The application-level protocol used by the client and the server, e.g., HTTP, FTP, and telnet.
- Hostname: The DNS Domain name (e.g., www.github.com) or IP adress (e.g., 192.128.1.2) of the server.
- Port: The TCP port number that the server is listening for incoming requests from the clients.
- Path-and-file-name: The name and location of the requested resource, under the server document base directory.
