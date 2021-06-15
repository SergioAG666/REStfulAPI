# REStfulAPI 

## Overview

Implementation of Test Cases: CRUD Pattern, for a pet store sample hosted at http://localhost:8080/. 

This is a java project to build a stand-alone server and other project which implements REST Assured. 

REST Assured is an open-source (free) Java library available for testing primarily the RESTful web services. 

REST Assured is a Java domain-specific language (DSL) for simplifying testing of REST-based web services built on top of HTTP. 

It supports most commonly used HTTP verbs like GET, POST, PUT/PATCH DELETE, OPTIONS, HEAD which can be used to validate & verify the response of these requests.

This demo shows a complete design using the CRUD pattern, where we can modularize and separate the data layer, API calls, test codes. 

##Test Cases Proposed
These **test cases** were oriented towards handling the **pets** option. First we created one pet, update this pet, get the pet, update the pet and the last operation is delete the pet.

They **test cases** are completely designed independent of the testing framework. This allows for code reuse, modularity, and better code maintenance.



_Dependency Details_

**io.rest-assured**      --> Rest Assured for testing API interactions(request & response),extract json/xml path.
**org.testng**           --> Designing the Test Frmework using TestNG Classes.
**com.google.code.gson** --> Represent the request body data in the from of java objects like Map <--> JSONformat.
**com.github.javafaker** --> To supply fake data for testing while sending request.
**com.jayway.jsonpath**  --> Extract data specifically from JSON file using jayway jsonpath.

_environment.java_ class to register all the available services with end-points
_petEndpoints.java_ class to perform Create, Read, Update, Delete requests to the services using the above-created end-points
_pet.java_ class to represents the data structure of the user payload which is in JSON format
_testPets.java_ class to perform the API Testing for the services using the TestNG class



To run web page, object under test (with Maven)
To run the server, run this task:

```
mvn package jetty:run
```

This will start Jetty embedded on port 8080.


Testing the server
Once started, you can navigate to http://localhost:8080/api/v3/openapi.json to view the Swagger Resource Listing. 

This tells you that the server is up and ready to demonstrate Swagger.

Using the UI
There is an HTML5-based API tool bundled in this sample--you can view it it at http://localhost:8080. This lets you inspect the API using an interactive UI. You can access the source of this code from here


To run test framework project
Download the project from github (https://github.com/SergioAG666/REStfulAPI.git)
Run the testPets.java class as TestNG test to observe results of tests. Each time you run the code, a different petId and petName is generated by the Java Faker class.