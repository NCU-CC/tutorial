# Build

this section is talking about the tool to **build** an application

## Table of Contents
- [Builds](#Builds)
- [Build-Tools](#Build-Tools)
- [Build-Task-Examples](#Build-Task-Examples)
- [Build-Examples](#Build-Examples)
- [References](#References)

## Builds
The procedure of building an application varies from team to team.
If we execute these steps by our own, we may waste too much time in such nonproductive tasks.

## Build-Tools
- Gradle : Groovy based DSL build system for the `JVM`
- Rake : Make-like program implemented in `Ruby`
- MsBuild : XML based platform for for `.NET` and `Visual Studio`
- Gulp : streaming build system for `frontend development`

## Build-Task-Examples
- Compile : specify target files to be compiled and destination to be placed
- Package : specify target files to be packaged and how to pack them
- Test : specify target tests to be executed and how to run them
- Deploy : specify the target server to be deployed and how to deploy

## Build-Examples
If you are building a backend Java Service in a big team, the task manager should write a build file for `Gradle`. This build file contains the setting of `how to build`, `where to build`, `how to test` and `how to package` so that the other developers can easily use these tasks to build on their computer or central CI server.

In situation of CI integrated, all commits can be built and verified on CI. After all tests are passed on CI, CI may use package task to pack them into `.war` file then try to deploy to target server.

**Build file may vary from different environments**

## References
- https://github.com/gradle/gradle
- https://github.com/ruby/rake
- https://github.com/microsoft/msbuild
- https://github.com/gulpjs/gulp
