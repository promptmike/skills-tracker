# HTTP in Detail

## Task 1 - What is HTTP(S)?

### What is HTTP? (HyperText Transfer Protocol)

HTTP is the set of rules used to communicate with web servers.
HTTP was developed by Tim Berners-Lee in 1989-1991 to transfer data from servers to clients.

### What is HTTPS? (HyperText Transfer Protocol Secure)

HTTPS is a secure version of HTTP that encrypts data for privacy and authentication of identity (you know which server you are accessing).
HTTP is the set of rules used to communicate with web servers, while HTTPS adds secure encryption practices to those rules.

## Task 2 - Requests And Responses

URLs are required to tell your browser exactly how and where to look for the data you request.
HTTP is the set of rules used to communicate with web servers, HTTPS adds secure encryption and URLs tell your browser where to find the server.

### What is a URL? (Uniform Resource Locator)

URLs take the form `scheme://user:password@subdomain.host-domain.tld:port#/path?id=query#fragment`.
HTTP is the rules for communicating with web servers, HTTPS adds secure encryption and URLs provide the location of the data according to rules.

The Scheme is the protocol to be used for fetching data (e.g. HTTP, HTTPS, FTP, etc).
A URL instructs the browser on how and where to find data on web servers according to a Scheme.

The User is the username and password to be used for authentication if the service requires it.
A URL instructs the browser on how and where to find data according to a Scheme, with the option to authenticate with User.

The Host is the domain name or IP Address of the service you wish to access.
A URL instructs the browser on how and where to access a Host according to a Scheme, with the option to authenticate the User.

The Port is the port number through which you will access the service (usually 80 for HTTP, 443 for HTTPS and 21 for FTP).
A URL shows how to access a service from a Host on a Port according to a Scheme with the option to authenticate the User.

The Path is the location of the resource you wish to access on the server.
URLs specify the Path to a resource on a Host accessed through a Port according to a Scheme with the option to authenticate the User.

The Query string gives additional information to the server on which resource you wish to access (e.g. /blog?id=1 for for article 1).
URLs can Query the Host to get resources from a Path through a Port according to a Scheme for an authenticated User.

The Fragment points to a specific element ID on a page.
URLs can Query the Host to get a Fragment of a page at a specific Path on the Host accessed through a Port according to a Scheme for a User.

### Making a Request

It is possible to make a Request to a web server with just one line - GET / HTTP/1.1 (the request method and protocol version).
Web servers can be accessed using URLs and Requests sent to them can be simple or complex.

For a richer web experience your Requests should include Headers to provide extra information to the web server.
Web servers can be accessed using URLs and will return data in response to Requests and the Headers they contain.

#### Example Request

__GET / HTTP/1.1__

__Host: tryhackme.com__
__User-Agent: Mozilla/5.0 Firefox/87.0__
__Referer: https://tryhackme.com/__

Line 1 sends the GET Method requesting the home page with "/" and specifies that HTTP version 1.1 is the protocol to be used.
Web servers can be accessed with URLs and sent requests for data using Methods such as GET.

Line 2 tells the server that the website tryhackme.com is what we want to access.
Web servers can be accessed with URLs and sent requests for data using Methods such as GET to access services such as a website.

Line 3 tells the server that we are using the Firefox 87 browser.
Web servers can be accessed with URLs and sent requests for data which can include additional information such as the browser we are using.

Line 4 tells the server that https://tryhackme.com/ is the page that refered us to this one.
Web servers can be accessed with URLs and sent requests which can include additional information such as the browser or referrer.

Line 5 is blank, because an HTTP request always ends with a blank line to tell the server we are finished.
Web servers can be accessed with URLs and sent requests which can include additional information to help them serve us the data we want.

#### Example Response:

HTTP/1.1 200 OK

Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98

`<html>`
`<head>`
`<title>TryHackMe</title>`
`</head>`
`<body>`
Welcome to TryHackMe.com
`</body>`
`</html>`

Line 1 tells us the protocol being used for the Response and gives us the 200 OK code to let us know the Request was successful.
Web servers are accessed with URLs and Respond to Requests using codes to let us know what happened to the Request.

Line 2 tells us the web server software and version number.
Web servers are accessed with URLs and Respond to Requests using codes to let us know what happened and providing additional information.

Line 3 gives us the current date, time and timezone of the web server.
Web server Responses give us additional helpful information such as protocol, status code and time/date/timezone.

Line 4 is the Content-Type Header, which tells us what kind of informationa is going to be sent in the Response.
Web server Responses contain Headers with additional helpful information about the server and the information it is about to send.

Line 5 is the Content-Length, which tells the client how long the Response is so we can confirm no data is missing.
Web server Responses contain useful Headers that tell us about the server and help us confirm no data is missing.

Line 6 is left blank to confirm the end of the HTTP Response.
Web server Responses contain Headers with useful information about the server and the data being sent, including a blank line to end.

Lines 7-14 are the information that was requested - in this case a homepage.
Web server Responses give us useful information about the server and the data being sent, followed by the data itself.

## Task 3 - HTTP Methods

HTTP Methods show the client's intended action when making a Request.
Web servers Respond with Headers and data to Requests made with Methods that show the client's intended action.

The GET Request is used for getting information from a web server.
Web servers Respond to Request Methods to provide data for the client.

The POST Request submits data to the server, potentially creating new records.
Web servers Respond to Request Methods by serving or receiving data to provide a service to the client.

The PUT Request submits data to the server to update information.
Web servers Respond to Request Methods by sending data, creating new records or updating records to provide a service to the client.

The DELETE Request deletes information/records from the server.
Web servers Respond to Request Methods by sending requested data, creating new records, updating records or deleting records for the client.

## Task 4 - HTTP Status Codes

### HTTP Status Codes:

There are 5 different ranges of HTTP Status Codes, which all inform the client of the outcome of their Request.
Web servers Respond to Request Methods by sending and receiving data, with HTTP Status Codes to inform the client of the outcome.

The first range (100-199) is Information Response, telling the client the first part of their request was successful.
Web servers Respond to Request Methods with data and send HTTP Status Codes to show the outcome, e.g. an Information Response.

The second range (200-299) is Success, telling the client their Request was successful.
Web servers Respond to Request Methods with data and send HTTP Status Codes to show the outcome, e.g. a Success code.

The third range (300-399) is Redirection, redirecting the client's Request to another resource.
Web servers Respond to Request Methods with data and send HTTP Status Codes to show the outcome, e.g. Redirect to another resource.

The fourth range (400-499) is Client Errors, telling the client there was an error with their Request.
Web servers Respond to Request Methods with the requested data if possible, but provide Status Codes in any case to show the client the outcome.

The fifth range (500-599) is Server Errors, telling the client there was an error with the server handling the Request.
Web servers Respond to Request Methods with the requested data if possible, providing Status Codes to help the client by showing the outcome.

### Common HTTP Status Codes:

There are many HTTP Status Codes and applications can even define their own.
Web servers Respond to Request Methods with requested data if possible, and can provide many Status Codes to show the outcome.

200 - OK tells us the Request was completed successfully.
Web servers Respond to Request Methods with requested data if possibleand common Status Codes show the outcome, e.g. 200 - OK for success.

201 - Created tells us that a new resource was successfully created, such as a new user or blog post.
Web servers tell us the outcome of Requests using Status Codes, such as 200 - OK for success or 201 - Created for new resource.

301 - Moved Permanently tells us that the requested resource has been moved somewhere else and we should look there instead.
Web servers show the outcome of Requests using Status Codes such as 200 for success, 201 for new resource or 301 for permanent redirect.

302 - Found tells us that the requested resource has moved, but unlike 301 this may be a temporary move.
Web servers show the outcome of Requests using Status Codes such as 201 for a new resource, 301 for permanent move or 302 for temporary move.

400 - Bad Request tells the client something was wrong with their Request (e.g. missing a parameter required by the resource we want).
Web servers show the outcome of Requests using Status Codes to help us troubleshoot problems.

401 - Not Authorised tells the client they are not allowed to access the resource requested until you have authorised (e.g. logging in).
Web servers protect resources against unauthorised access and send Status Codes to help us troubleshoot problems.

403 - Forbidden tells the client they are not allowed to access the resource requested even if logged in.
Web servers protect resources against unauthorised or improper access and send Status Codes to help us troubleshoot problems with Requests.

405 - Method Not Allowed tells us the Method used for the Request is not allowed for this resource (e.g. sent a GET when POST is required).
Web servers provide and protect resources, Respond to Requests and provide Status Codes to help us troubleshoot Request problems.

404 - Page Not Found tells us the resource we requested does not exist.
Web servers Respond to Requests for resources, send data to those authorised and provide Status Codes to help us troubleshoot Request problems.

500 - Internal Service Error tells us the server has encountered an error that it does not know how to handle.
Web servers Respond to Requests for resourses, exchange data with those authorised and provide Status Codes to help us troubleshoot errors.

503 - Service Unavailable tells us the server cannot handle the request as it is too busy or down for maintenance.
Web servers Respond to authorised Requests and send Status Codes to help us troubleshoot client-side errors or show server-side errors.

Visit http.cat for a memorable list of HTTP Status Codes.
Web servers Respond to Requests from authorised clients and provide Status Codes for server-side or client-side errors.

## Task 5 - Headers

You can put additional information in Headers when making Requests.
Web servers take Requests and Headers in Requests and Respond to authorised clients with data and Status Codes.

HTTP Requests do not **require** headers, but you will have difficulty viewing a website properly without them.
Web servers take Requests, usually with Headers, and Respond to authorised clients with data and Status Codes for troubleshooting.

### Common Request Headers

Common Request Headers are sent from the client to the server.
Web servers take Requests, usually with Headers, from clients and return data to those authorised to access it.

The Host Header tells the server which site you want, otherwise you will receive the default site for the server.
Web servers can host multiple sites and take Requests from clients with Headers to explain what they want to access.

The User-Agent Header tells the server which browser you are using so that it can format the site in the best way for you.
Web servers can host multiple services and take Requests with Headers that explain what the client wants to access and how.

The Content-Length Header tells the server how long the Request is so that it can check there is nothing missing.
Web servers take Requests with Common Request Headers that allow error-checking and explain what the client wants to access and how.

The Accept-Encoding Header tells the server what types of compression the browser will accept so that the data can be made smaller for transit.
Web servers take Requests with Common Request Headers that allow error-checking and help the server provide the correct data for the client.

The Cookie Header provides information that the client wants the server to remember.
Web servers respond to Common Request Headers by error-checking, providing a specific service, formatting and encoding data and keeping cookies.

### Common Response Headers

Common Response Headers are returned to the client from the server after a Request.
Web servers receive Common Request Headers and return Common Response Headers.

The Set-Cookie Header provides information for the client to store and send back to the server in subsequent Requests.
Web servers receive Common Request Headers and return Common Response Headers with information such as cookies for the browser to store.

The Cache-Control Header tells the client how long to store the Response in its browser cache before requesting it again.
Web servers receive Common Request Headers and return Common Response Headers with information such as how long to store a page in cache.

The Content-Type Header tells the client what type of data is being sent in the Response (e.g. HTML, PDF, MP4, etc) so the browser can process it.
Web servers receive Common Request Headers and return Common Response Headers with information such as caching time or content type.

The Content-Encoding Header tells the client what compression method has been applied to the Response data so we know how to decompress it.
Web servers receive Common Request Headers and return Common Response Headers with information such as encoding, content type and caching time.

## Task 6 - Cookies

HTTP is stateless, so cookies are stored and sent with each request to remind the server of information about the client.
Web servers receive Common Request Headers, return Common Response Headers and give cookies to browsers to send back with future Requests.

__GET / HTTP/1.1__
__Host: cookies.thm__
__User-Agent: xxxx__

The client Requests the web page from cookies.thm in this example.
Web servers receive Common Request Headers and return Common Response Headers, also providing browser cookies to send with future Requests.

__HTTP/1.1 200 OK__
__Server: nginx/1.15.8__
__Date: Wed, 14 Apr 2021 09:08:19 GMT__
__Content-Type: text/html; charset=UTF-8__

__HTML DATA.....__

The server tells us the Request was successful and Responds with a simple web page containing a form asking for the user's name.
Web servers receive Common Request Headers and return Common Response Headers in their Responses, along with cookies to remember the user.

__POST / HTTP1.1__
__Host: cookies.thm__
__User-Agent: xxxx__
__Content-Type: application/x-wwwform-urlencoded__
__Content-Length: 9__

__name=adam__

The client sends back the form in a POST Request with the name field set to "adam".
Web servers receive Common Request Headers and return Common Response Headers with the requested data and cookies for future reference.

__HTTP/1.1 200 OK__
__Server: nginx/1.15.8__
__Date: Wed, 14 Apr 2021 09:08:19 GMT__
__Set-Cookie: name=adam__
__Content-Type: text/html; charset=UTF-8__

__HTML DATA.....__

The server Responds to the form with a Set-Cookie Header instructing the client to save the data "name=adam" as a cookie.
Web servers receive Common Request Headers and return Common Response Headers including Set-Cookie Headers with data for the browser to save.

__GET / HTTP/1.1__
__Host: cookies.thm__
__User-Agent: xxxx__
__Cookie: name=adam__

The client sends the saved data back to the server in a Cookie Header, and continues to do this with future Requests.
Web servers receive Common Request Headers including Cookie and return Common Response Headers including Set-Cookie to provide data to save.

__HTTP/1.1 200 OK__
__Server: nginx/1.15.8__
__Date: Wed, 14 Apr 2021 09:08:19 GMT__
__Content-Type: text/html; charset=UTF-8__
__`<html><body>`Welcome back adam`</body></html>`__

The server receive the cookie in the Request and instead of displaying the form it displays the welcome back message with the user's name.
Web servers provide cookies in Set-Cookie Headers which clients can return in Cookie Headers which then inform the Response of the server.

Cookies can be used for many things, but most commonly they are used for authentication by storing a token (not the actual password).
Web servers provide cookies in Set-Cookie Headers which clients return in Cookie Headers to keep persistent information such as authentication.

### Viewing Your Cookies

You can view the cookies your browser is sending to a website using the developer tools.
Web servers provide cookies in Set-Cookie Headers which browsers return in Cookie Headers and the user can view in developer tools.

In developer tools you can select the Network tab to see Requests and view cookies in the Cookie tab of each Request (if sent).
Web servers provide cookies in Set-Cookie Headers which browsers return in Cookie Headers of Requests which can be seen with developer tools.

## Task 7 - Making Requests

Use the Emulator to make HTTP Requests.
HTTP is a protocol to send and receive data with Header for additional information and cookies to keep information persistent statelessly.