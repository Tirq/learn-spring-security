# spring-securing-web-application
This guide walks you through the process of creating a simple web application with resources that are protected by Spring Security. This example is based on the Spring guides, available in https://spring.io/guides/gs/securing-web/. 

## Build and Run project
To build this project, you need to have Gradle installed in your system because I decided to not use the Gradle wrapper commands.

In the root of the project execute:
```
gradle build
```
And then to start the embedded server execute:
```
java -jar build/libs/five-secure-web.jar
```
The name of the jar is declared in the _build.gradle_ file in the _bootJar_ section. 

## Authentication

This project shows how to use the Spring Security to create authentication in a MVC web application. 
There are two public pages: _home_ and _login_ and a private page: _hello_. 

The pages are using _Thymeleaf_ as a template. 
It was necessary to create two classes to enable the functionalities: 

1. _MvcConfig_: Configurations about the pages HTML.
2. _WebSecurityConfig_: Configurations about what pages are public and what are private. 

Also, it was create a User in memory to easily use the system.