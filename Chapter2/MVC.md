# MODEL-VIEW-CONTROLLER

this section is talking about Model, View, Controller architecture

## Table of Contents
- [MVC](#http)
- [Model](#model)
- [View](#view)
- [Controller](#controller)
- [Examples](#examples)
- [References](#references)

## MVC
MVC ( Model View Controller ) is a kind of software architecture.

It splits the **UI** and **business logic** into three parts:

- Model
- View
- Controller

There are many versions of MVC definition. And we are talking about the **Model2** here.

Model2 is a specific design for web application.

### MVC Procedure

Requests are passed to the controller.

The **controller** performs any logic necessary to obtain the correct content from model.

The **model** contains business logic to process data.

The controller pass processed data to **view** to render the response.

### MVC Frameworks
- Ruby on Rails
- Laravel
- Django

## Model
The model contains all business logic

### Model Examples
- Database Operations
- Action Policies

## View
The view renders the data

### View Examples
- Render HTML
- Render JSON

## Controller
The controller processes requests and passes data from specific model to specific view

## Examples
A client wants to get the specific user data :

1. request is passed to **controller**

    ![mvc](./images/mvc-01.jpg)

- **controller** checks its request format

    ![mvc](./images/mvc-02.jpg)

- **controller** calls **model** to get specific user data

    ![mvc](./images/mvc-03.jpg)

- **model** connects to the database then reads data

    ![mvc](./images/mvc-04.jpg)

- **controller** passes the data to **view**

    ![mvc](./images/mvc-05.jpg)

- **view** render the user data in JSON

    ![mvc](./images/mvc-06.jpg)

- response is passed to the client

    ![mvc](./images/mvc-07.jpg)

## References
- https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller
- http://blog.turn.tw/?p=1539
