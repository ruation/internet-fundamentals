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

## HTTP Messages

HTTP client and server communicate by sending text messages. The client sends a request message to the server. The server, in turnm returns a response message.

An HTTP message consists of a message header and an optional message body, separated by a blank line, as illustrated below:

```hhhhhhhhhhhhhhh |
hhhhhhhhhhhhhhh | ➡️ Message Header
hhhhhhhhhhhhhhh |
                  ➡️ A blank line separates the header and body
bbbbbbbbbbbbbbb |
bbbbbbbbbbbbbbb |
bbbbbbbbbbbbbbb | ➡️ Message Body (optional)
bbbbbbbbbbbbbbb |
**HTTP Messages**
```

 **Request message (from your browser to the server):**

```
 GET /doc/test.html1 HTTP/1.0         ← Request Line       |
 Host: www.test10.com                 |                    |
 Accept: image/gif, image/jpeg, */*   |                    |  Request
 Accept-Language: en-us               |- Request Headers   |- Message
 Accept-Encoding? gzip, deflate       |                    |  Header
 User-Agent: Mozilla/4.0              |                    |
 Content-Length: 45                   |                    |
                                      ← A blank line separates header and body
 bookId=54321&author=Ru+Ã+N           ← Request Message Body
 ```

**HTTP Response Message:**

```
HTTP/1.1 200 OK                      ← Status Line         |
Date: Sun, 10 Aug xxxx 09:32:11 GMT  |                     |
Server: Apache/1.3.29 (Win32)        |                     |  Response
Last-Modified: Sun, 10 Aug xxxx       |                     |  Message
Etag: "0-26-1008r10l9"               |- Response Headers   |- Header
Accept-Ranges: bytes                 |                     |
Content-Length: 45                   |                     |
Connection: open                     |                     |
Content-Type: text/html              |                     |
                                     ← A blank line separates header and body
<h1>My github repository</h1>        ← Response Message Body
```

## Request Methods

- **GET**: A client can use the GET request to get a web resource from the server.
- **HEAD**: A client can use the HEAD request to get the header that a GET request would have obtained. Since the header contains the last-modified date of the data, this can be used to check against the local cache copy.
- **POST**: Used to post data up to the web server.
- **DELETE**: Ask the server to delete the data.
- **TRACE**: Ask the server to return a diagnostic trace of the actions it takes.
- **OPTIONS**: Ask the server to return the list of request methods it supports.
- **CONNECT**: Used to tell a proxy to make a connection to another host and simply reply the content, without attempting to parse or cache it. This is often used to make SSL connection through the proxy.
