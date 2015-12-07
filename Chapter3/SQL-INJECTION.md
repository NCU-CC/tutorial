# SQL INJECTION
this section is talking about sql injection fundamental

**If you have not been familiar with SQL, you can pass this section temporily**

## Table of Contents
- [SQL-Injection](#SQL-Injection)
- [SQL-Injection-Examples](#SQL-Injection-Examples)
- [SQL-Injection-Prevention](#SQL-Injection-Prevention)
- [References](#References)

## SQL-Injection
SQL injection is a **code injection** technique, used to attack data-driven applications, in which `malicious SQL statements are inserted into an entry field for execution`

## SQL-Injection-Examples
  1. Let's suppose that this is a authentication SQL of a website
    ```sql
    strSQL = "SELECT * FROM users WHERE (name = '" + userName + "') and (pw = '"+ passWord +"');"
    ```
    where `userName` and `passWord` are strings from user input

  - If an attacker type following contents the in the form
    ```sql
    userName = "1' OR '1'='1";
    passWord = "1' OR '1'='1";
    ```
  - The operation above would lead to
    ```sql
    strSQL = "SELECT * FROM users WHERE (name = '1' OR '1'='1') and (pw = '1' OR '1'='1');"
    ```
    which equals to
    ```sql
    strSQL = "SELECT * FROM users;"
    ```
  - The attacker can now pass the user authentication


## SQL-Injection-Prevention
- Parameterized statements

  ```sql
  SELECT * FROM users WHERE name = ? and pw = ?
  ```
  `first ?` and `second ?` must be treated as a plain text instead of SQL statement

- Escaping

  find out all `'` characters in inputs then replace them by `''`

- Pattern check

  `Integer`, `float` or `boolean`, string parameters can be checked if their value is valid representation for the **given type**

- Database permissions

  Limiting the permissions on the database used by the web application to only what is needed

## References
- https://en.wikipedia.org/wiki/SQL_injection
