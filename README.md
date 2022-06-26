
# Web Application
## Prerequisites
This project would require **Java 8** and **Maven** to be set up.  
To set up maven use the tutorial in the link : https://www.baeldung.com/install-maven-on-windows-linux-mac

## Technology Stack
### 1. Operating System
* Linux based Operating System - Ubuntu
### 2. Programming Language
* Java 8
### 3. Relational Database
* MySQL
### 4. Backend
* Spring Boot
* Maven
### 5. Testing
* JUnit
* Mockito
* REST-assured

## Build Instructions
  
### Start mysql server
`systemctl start mysql`

### Start the backend server
Navigate to webapp folder  
`cd webapp`<br><br>
Run the following command

### For Default profile
`./mvnw spring-boot:run -Dspring-boot.run.profiles=default -Dspring-boot.run.arguments=--spring.bucket.name=*bucket-name*`

### For Dev profile
`./mvnw spring-boot:run -Dspring-boot.run.profiles=dev -Dspring-boot.run.arguments=--spring.bucket.name=*bucket-name*,--spring.datasource.url=jdbc:mysql://*endpoint-url*/csye6225`

## Deploy Instructions

### Technology
* AWS CodeDeploy

## Database
**MySQL** and **JPA** required.

## Environment Variables or VM arguments.
	 salt=<salt>
	 dbpwd=<database-Password>
Please enter it as in your VM arguments
````
salt=mysalt;dbpwd=mypassword
````


## Steps to run the application.
Use the command line/terminal to navigate to the project folder.

- To build use
```  
mvn --batch-mode --update-snapshots install ```  
- To run tests  
```  
mvn --batch-mode --update-snapshots test
```  
- To start the application  
```  
cd target  
java -jar assignment-1.0-SNAPSHOT.jar
```  
  
The url to check the health would be http://localhost:8081/healthz
