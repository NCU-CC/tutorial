# CSRF-ATTACK
this section is talking about csrf attack and its prevention

**If you have not been familiar with HTML / HTTP, you can pass this section temporily**

## Table of Contents
- [CSRF](#csrf)
- [CSRF-Examples](#csrf-examples)
- [CSRF-Prevention](#csrf-prevention)
- [CSRF-XSS](#csrf-xss)
- [References](#references)

## CSRF
CSRF ( Cross-site request forgery ) is a type of malicious exploit of a website whereby **unauthorized commands are transmitted from a user that the website trusts**

## CSRF-Examples
1. If a bank transfer money by a url  `http://www.examplebank.com/withdraw?amount=A&for=B`
  - A is the amount to transfer
  - B is the target account name


2. An attacker send a link to victims via email
`http://www.examplebank.com/withdraw?amount=1000&for=AttackerAccount`

3. Any logged in victim click the link would send $1000 to AttackerAccount

## CSRF-XSS
- XSS exploits the trust a user has for a particular site
- CSRF exploits the trust that a site has in a user's browser

## CSRF-Prevention
- Synchronizer Token Pattern
  1. Server generate a unique secret token and bind it to user session
  2. Server render the form with that token
  ```html
  <input type="hidden" name="csrfmiddlewaretoken" value="KbyUmhTLMpYj7CD2di7JKP1P3qmLlkPt" />
  ```
  3. When client request comes, check the request token with the session token
    - same as session token : valid request
    - different from session token : invalid request
  4. destroy the token in session  


## References
- https://en.wikipedia.org/wiki/Cross-site_request_forgery
- https://github.com/astaxie/build-web-application-with-golang/blob/master/zh/09.1.md
