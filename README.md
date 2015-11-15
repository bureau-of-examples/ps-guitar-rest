Notes
============
Just like Spring Data JPA makes the underlying data source available to JPA clients, Spring Data Rest makes the underlying Spring data repositories (e.g. Spring Data JPA repositories) available to REST clients via a REST web service.

Setting up spring-data-rest in a spring-boot project is very simple if spring-data-jpa repositories have been correctly set up .
Just add the Maven dependency for spring-data-rest:
```xml
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-rest</artifactId>
		</dependency>
```

and in <code>application.properties</code> set the base uri to access the repositories:
<pre>
spring.data.rest.base-uri=/api
</pre>

Then run the project as a Java application (spring-boot application) and access: 
http://localhost:8080/api/

Spring Data Rest automatically exposes the available hyperlinks to the rest resources.


ps-guitar-rest
============

A Basic Spring Data JPA app with an H2 DB running on Spring Boot

Prerequisites
-------------
You will need to following tools in order to work with this project and code

* git (http://git-scm.com/)
* JDK 1.8+ (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Maven 3.x+ (http://maven.apache.org/)
* An IDE of your choice.  (Eclipse, IntelliJ, Spring STS, Netbeans, etc.)

Getting Started
---------------
To run this project locally, perform the following steps.

* Clone project to your machine using git - "git clone https://github.com/dlbunker/ps-guitar-rest.git"
* Import the project into your IDE using the maven pom.xml.  In spring STS suite this is done by importing an existing maven project
* Run the JUnit tests in the src/test/java folder.  If all the tests pass, pat yourself on the back.
* Next try running the app as a Spring Boot app.  You can do this by running the Main.java file in this project as a standard java project or you can run spring boot at your project's root with Maven using the following command.  'mvn spring-boot:run'
