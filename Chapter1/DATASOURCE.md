# DATASOURCE
this section is talking about where the data comes from in web services

## Table of Contents
- [Web-DataSource](#Web-DataSource)
- [From-Request](#From-Request)
- [From-File](#From-File)
- [From-Database](#From-Database)
- [From-Other-Services](#From-Other-Services)
- [References](#References)

## Web-DataSource
Data is very important in web service because we can't do anything without data!
The following are some examples of data source.

## From-Request
Data is not at server side but client side, so the data must be in requests

### From Request Examples
- calculate values
  - request
        GET /api/math/square?value=5

  - response
        {
          "value" : 5,
          "square" : 25
        }

- random number
  - request
        GET /api/math/random?type=int&min=0&max=10

  - response
        {
          "random" : 6
        }


## From-File
Data comes from the file system at server side

### From File Examples
- file upload
  - request
        POST /api/files
        [ your file data ]

  - response
        200 OK
        {
          "id" : "ABC123"
        }

- web page
  a simple web server which serve static html pages

## From-Database
Data is saved in databases and server can read these data from DBMS.

### What is Database
A database is an organized collection of data

### What is DBMS
A database management system ( DBMS ) is a application that interacts with the user, other applications, and the database itself to capture and analyze data

### From Database Examples
- user authentication
  1. all user data is saved in database
  - a user tries to login to a website
  - the server connect to DBMS to read corresponding user data
  - the server validates user certificate by data in databse
  - the server let user in if the data is matched

## From-Other-Services
Data can be fetched from other connected web services

### From Other Services Examples
- Proxy Server

## References
- https://developers.google.com/drive/web/manage-uploads
- https://en.wikipedia.org/wiki/Database
