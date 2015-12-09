# Migration

this section is talking about database data and schema management in application development

## Table of Contents
- [Migrations](#migrations)
- [Migration-Tools](#migration-tools)
- [Migration-Examples](#migration-examples)
- [References](#references)

## Migrations
Migrations are like version control for your database, allowing a team to easily modify and share the application's database schema.

```
There is only one data set so we shall make sure the consistency of data !
```

## Migration-Tools
- Flyway : schema migration for JVM
- Liquibase : schema migration for JVM

## Migration-Examples
Multiple developers work on same application and they both modify the schema of database. If they don't have migration tool, they need to modify the database by their own.
Big trouble may occurred in the case of error modifying database.

If they use migration management tool, they can write down each change of the database and let the tool manage them. When migration tool is executed, it would check for the state of database and try to migrate if necessary.

## References
- http://laravel.com/docs/5.1/migrations
