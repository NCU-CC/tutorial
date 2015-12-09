# WEB-AUTH

this section is talking about user / client authentication and authorization in web

## Table of Contents
- [Authentication](#authentication)
- [Web-Authentication](#web-authentication)
- [Authorization](#authorization)
- [Web-Authorization](#web-authorization)
- [References](#references)

## Authentication
Authentication is a series of procedure to verify the user identity

### Authentication Examples
- a school authenticates students by student cards
- a security system authenticates person by fingerprint

## Web-Authentication
Web server also needs a way to find out who you are

### Web Authentication Examples

- authenticate user using Cookie
  1. a user agent has the user certificate in cookie
  - the user visits a website with that cookie
  - the website validates the cookie
  - the website let the user in if certificate is valid


- authenticate user using token
  1. the user certificate is represented by a token
  - the user visits an web service using that token
  - the web service validates the token
  - the web service returns the result if certificate is valid

## Authorization
Authorization determine who is allowed to do what

### Authorization Examples
- a teacher authorizes you to enter that room
- a company authorizes you to read secret data

## Web-Authorization
We are talking about the 3rd party authorization here

### Web Authorization Examples
- OAuth
  1. a user launches a facebook app
  - the app redirects you to facebook page
  - facebook asks you for authorizing the app to get your data
  - the app gets a token if the user confirmed
  - the app can access the user facebook data by access token


## References
- http://stackoverflow.com/questions/6556522/authentication-versus-authorization
- http://oauth.net/2/
- http://openid.net/connect/
