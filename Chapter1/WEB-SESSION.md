# WEB-SESSION

this section is talking about state persistent in web

## Table of Contents
- [Cookie](#Cookie)
- [Session](#Session)
- [References](#References)

## Cookie
Cookie is a string stored in user agent ( browser ) to maintain the state between client / server

### Cookie in Response
When a response received, Cookie would be sent to client by `Set-Cookie` header

    HTTP/1.0 200 OK
    Content-type: text/html
    Set-Cookie: theme=light

### Cookie in Request
When a request launched, Cookie would be sent to server by `Cookie` header

    GET /spec.html HTTP/1.1
    Host: www.example.org
    Cookie: theme=light

### Cookie Examples
- shopping cart
- auto login

### Cookie Headers
header      |  type      | description | example
-----       |  -------   | ----------- | ----
Cookie      | request    | get cookie content | Cookie: `$Version=1; Skin=new;`
Set-Cookie  | response   | set cookie content | Set-Cookie: `UserID=JohnDoe; Max-Age=3600; Version=1`

### Cookie Disadvantage
- cookie is sent in each request so that the packet size may increment
- cookie is restricted in a small size
- cookie is sent in clear text unless use HTTPS

## Session
Session is a string stored in server to maintain the state between client / server

Session is implemented by Cookie in most of all cases

### How Session Works
Server wants to store some client-specific information in server instead of client,
but HTTP is stateless so that server needs a way to recognize each client.
To resolve this, server can sent an ID representing each client to client using Cookie.
Whenever server receive the Cookie, server would know what does the ID mean for and find corresponding data.

### Session in Response
When a response received, Session ID would be sent to client by `Set-Cookie` header

    HTTP/1.0 200 OK
    Content-type: text/html
    Set-Cookie: SESSIONID=123456

**p.s.** this `SESSIONID` text may vary with different server

### Session in Request
When a request launched, Session ID would be sent to server by `Cookie` header

    GET /spec.html HTTP/1.1
    Host: www.example.org
    Cookie: SESSIONID=123456

**p.s.** this `SESSIONID` text may vary with different server

### Session Examples
- user authentication

### Session Disadvantage
- session may cause high memory consuming if use in-memory session

## References
- https://en.wikipedia.org/wiki/HTTP_cookie
- https://en.wikipedia.org/wiki/List_of_HTTP_header_fields
