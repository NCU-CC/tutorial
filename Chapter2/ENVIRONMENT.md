# Environment

this section is talking about different environment setting in application development

## Table of Contents
- [Environments](#Environments)
- [Development-Environment](#Development-Environment)
- [Test-Environment](#Test-Environment)
- [Production-Environment](#Production-Environment)
- [Examples](#Examples)

## Environments
In the progress of application development, we can simply split the environment into three parts:

- **Development** for developing
- **Test** for testing
- **Production** for real product

These environments contain different settings and services

## Development-Environment
The `development` environment is used for developing an application.

When you are developing, you may not build a full-featured environment ( e.g. `monitoring`, `caching`, `data compression` ).
Instead, you may build a simple server without exception capturing and all caching technique so that developer can know what happened in each step.

## Test-Environment
The `test` environment is used for testing.

This contains the minimum components only for running tests. For example, developer can use in-memory database instead of common database if possible to accelerate the test speed.

## Production-Environment
The `production` environment is used for real product.

It contains **all components**.

## Examples
- Development-Environment for development server
- Production-Environment  for production server
- Test-Environment for Continuous Integration Server
