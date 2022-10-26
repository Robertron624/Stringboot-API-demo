# Spring Boot API Demo

This project is a demo of a Spring Boot Resftul API to perform CRUD (Create, Read, Update and Delete) operations to a MySql database.

To start the project first you must edit rhe application.properties file inside src/main/resources, changing your datasource url, your database user and password, you need to also create a database in MySql Workbench.

Your datasource.url must look like this:

jdbc:mysql://{your database ip}:{port}/{database name}

After that just run the main function inside src/main/java/com/example/demo/DemoApplication.java.

## Create an user

Send a post request to: http://localhost:8080/api/v1/addUser

body of request:

    {
        "fname": "your user first name",
        "lname": "your user first name",
        "age": your users age (integer)
    }

## Get all users

Send a GET request to: http://localhost:8080/api/v1/users/

## Get user by Id

Send a GET request to: http://localhost:8080/api/v1/users/{id}

## Update user by Id

Send a PUT request to: http://localhost:8080/api/v1/updateUsers/

with this body:

    {
        "id": user id,
        "fname": "new user firstname",
        "lname": "new user lastname",
        "age": new user age (integer)
    }

## Delete user by Id

Send a DELETE request to: http://localhost:8080/api/v1/deleteUsers/{id}