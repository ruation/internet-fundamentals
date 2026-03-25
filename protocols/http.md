# Hypertext Transfer Protocol (HTTP)

Whenever you go to a site with a URL that use HTTP, e.g. "http://www.github.com/", your browser turn this into a request message and sends it to the HTTP server. The HTTP server interprets the request message, and returns you an appropriate response message, which is either the resource you requested or an error message. This process is illustrated bellow:

- User issues a URL from a browser, e.g. "http://www.github.com/"
- Browser sends a request message, e.g. "GET URL HTTP/1:1"
- Server maps the URL to a file or program under the document directory. 
- Server returns a response message, e.g. "HTTP/1.1 200 OK"
- Browser formats the response and displays

## Uniform Resource Locator (URL)

Is used to uniquely indentify a resource over the web.

**Syntax:**

protocol://hostname:port/path-and-file-name

- Protocol: The application-level protocol used by the client and the server, e.g., HTTP, FTP, and telnet.
- Hostname: The DNS Domain name (e.g., www.github.com) or IP adress (e.g., 192.128.1.2) of the server.
- Port: The TCP port number that the server is listening for incoming requests from the clients.
- Path-and-file-name: The name and location of the requested resource, under the server document base directory.

## Especifications

The HTTP especification is maintained by W3C (World-wide Web Consortiium) and available at http://www.w3.org/standards/techs/http.

- HTTP/0.9 (1991) - Original vesion, written by Tim Berners-Lee, simple protocol for transferring raw data across the internet.
- HTTP/1.0 (1996) - improved the older by allowing MIME-like messages.
- HTTP/1.1 (1999) - adress the issues of proxies, caching, persistent connection, virtual hosts and range download.

## HTTP Request and Response Messages

HTTP client and server communicate by sending text messages. The client sends a request message to the server. The server, in turnm returns a response message.

An HTTP message consists of a message header and an optional message body, separated by a blank line, as illustrated below:

'''hhhhhhhhhhhhhhh |
hhhhhhhhhhhhhhh | ➡️ Message Header
hhhhhhhhhhhhhhh |
                  ➡️ A blank line separates the header and body
bbbbbbbbbbbbbbb |
bbbbbbbbbbbbbbb |
bbbbbbbbbbbbbbb | ➡️ Message Body (optional)
bbbbbbbbbbbbbbb |
**HTTP Messages**
'''

The format of an HTTP request message is as follow:

'''
Request Line    <   hhhhhhhhhhhhhhh |
                  | hhhhhhhhhhhhhhh | ➡️ Request Message Header
Request Headers < | hhhhhhhhhhhhhhh |
                                      ➡️ Separated by a blank line
                    bbbbbbbbbbbbbbb |
                    bbbbbbbbbbbbbbb |
                    bbbbbbbbbbbbbbb | ➡️ Request Message Body (optional)
                    bbbbbbbbbbbbbbb |
                    bbbbbbbbbbbbbbb |
                    **HTTP Request Message**'''

## Request Line

The first line of the header is called the request line, followed by optinional request headers.

The request line has the following syntax:
'''request-method-name request-URI HTTP-version'''
