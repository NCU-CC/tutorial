# WEB-API

this section is talking about APIs

## Table of Contents
- [API](#API)
- [WEB-API](#WEB-API)
- [RESTFUL-API](#RESTFUL-API)
- [References](#References)

## API
API ( Application Programming Interface ) is a set of routines, protocols and tools for building software applications

### API Examples

- API in Unix System

          SYNOPSIS
                      #include <math.h>
                      double sqrt(double X);
                      float  sqrtf(float X);
          DESCRIPTION
                 sqrt computes the positive square root of the argument. ...
          RETURNS
                 On success, the square root is returned. If X is real and positive...


- API in Java programming language

          class Scanner
    
          public String nextLine()
    
            Advances this scanner past the current line and returns the skipped input...
    
          Returns:
    
            the line that was skipped
    
          Throws:
    
            NoSuchElementException - if no line found
    
            IllegalStateException - if this scanner is closed        


## WEB-API
WEB API is used for exchanging information with a website.
It typically consists of public endpoints  that accept HTTP requests and respond with requested data,
typically in the form of `JSON` or `XML`

### WEB API Examples

- Request

    ```
    GET /books/1
    Host: api.bookstore.com
    Accept: application/json
    ```
      

- Response

    ```
    HTTP/1.1 200 OK
    Content-Type: application/json
    Content-Length: xxx
    ```
    
    
    ```json
    {
        "id" : "1",
        "name" : "make a web api in 3 mins",
        "description" : "web api tutorial",
        "price" : 20
    }
    ```
    

## RESTFUL-API

### What is REST
REST ( Representational State Transfer ) is a software architectural style of web

- Individual resources are identified by URI

  `/books/1` `/books/2` `/projects/1/issues/1`

- Operations on resources correspond to HTTP status

  `GET /books/1` `DELETE /books/1` `PUT /books/1` `POST /books`

- Response type should be specified in HTTP header

  `Accept: application/json`  `Content-Type: application/xml`

### What is RESTful API
Any Web APIs that adhere to the REST architectural constraints ( SEE IN REFERENCE ) are called RESTful APIs

### RESTful Examples

resource : `http://api.bookstore.com/books`

method   |  description | example
-----    |  -------   | ----------
GET      | get all books | `GET /books` <br> `200 [ { "id" : 1, "name" : "Old School" } ]`
POST     | create a new book | `POST /books [ { "name" : "Good Days" } ]` <br> `201 { "id" : 2, "name" : "Good Days" }`

resource : `http://api.bookstore.com/books/1`

method   |  description | example
-----    |  -------   | ----------
GET      | get the book with id 1 | `GET /books/1` <br> `200 { "id" : 1, "name" : "Hello World" }`
PUT      | update the book with id 1 | `PUT /books/1 [ { "name" : "Hello World!!!" } ]` <br> `200 { "id" : 1, "name" : "Hello World!!!" }`
DELETE   | delete the book with id 1 | `DELETE /books/1` <br> `204`

## References
- https://en.wikipedia.org/wiki/Application_programming_interface
- https://en.wikipedia.org/wiki/Web_API
- https://en.wikipedia.org/wiki/Representational_state_transfer
- http://bbear.me/qian-hou-duan-fen-chi-tr/
