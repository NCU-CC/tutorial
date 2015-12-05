# Dependency

this section is talking about how to manage the dependencies of an application

## Table of Contents
- [Dependency-Management](#Dependency-Management)
- [Dependency-Management-Tools](#Dependency-Management-Tools)
- [Dependency-Management-Examples](#Dependency-Management-Examples)
- [References](#References)

## Dependency-Management
If we download and move each lib into out project folder, we may also waste too much time in such nonproductive tasks.
Developers should concern **"what I want"** instead of **"where is it"** !

The dependency management tool can manage all dependencies by its own, so the developers can keep focus on their missions.

This technique relies on remote lib repository and the configuration in each lib which specify all dependencies of it.

## Dependency-Management-Tools
- Maven : software project management and comprehension tool for the `JVM`
- NPM : a `JavaScript` package manager
- Bundler : manage application's gem `(ruby)` dependencies with less pain

## Dependency-Management-Examples
There are libraries **A**, **B** and **C** where
- A depends on B
- B depends on C

If we just want to use the API of **A**, we must have to download **B** and **C** or it would not work!
If we have dependency management tool, we can just tell it that we need **A**. Then it would analyze its dependencies and download them for us automatically.

## References
- https://maven.apache.org/
- https://github.com/npm/npm
- https://github.com/bundler/bundler
