# DEVELOPMENT-TOOL

this section is talking about tools for web application development

## Table of Contents
- [Development-Tool](#Development-Tool)
- [Environment](#Environment)
- [Version](#Version)
- [Build](#Build)
- [Dependency](#Dependency)
- [Migration](#Migration)
- [References](#References)

## Development-Tool
In order to develop a large web application, we cannot do without the help of automation tools.

It is for not only developers but also machines.

Almost all tools can be executed from terminal so that the automation system can trigger them without human.

## Environment
In the progress of application development, we can simply split the environment into three parts:

- **Development** :  developer's environment
- **Test** : specific environment for the purpose of test
- **Production** : real environment of this application

These environments contain different data or services to be used.

## Version
Version Control System has become the most important technique today.
If you always write codes in a 1 person team, then this may not work for you.
But if you are working in a huge team, it may be a nightmare without version control system.

Version Control System provides a way for users to work distributedly.
Users can write their own code and merge them in a simple way.

These are famous version control systems :
- **GIT**
- CVS
- SVN

## Build
The procedure of building an application varies from team to team.
If we execute these steps by our own, we may waste too much time in such nonproductive tasks.

To solve this problem, many build tools are invented :
- Gradle
- Rake
- MsBuild
- Gulp

These tools can manage tasks for the application such as
- Compile
- Package
- Test
- Deploy

## Dependency
If we download and move each lib into out project folder, we may also waste too much time in such nonproductive tasks.
Developers should concern **"what I want"** instead of **"where is it"** !

These dependency management tools can manage all dependencies by its own, so the developers can keep focus on their missions.

The followings are some dependency management tools :
- Maven
- NPM
- Bundler

## Migration
Migrations are like version control for your database, allowing a team to easily modify and share the application's database schema

```
There is only one code repository and so does the database !
```

Database migration tools example :
- Flyway
- Liquibase

## References
- http://laravel.com/docs/5.1/migrations
