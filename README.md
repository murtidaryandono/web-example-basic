# web-example-basic

---
### Table of contents
1. Version <br/>
2. Description <br/>
3. Technology stack <br/>
4. Architecture <br/>
5. Sequence diagram <br/>
6. Project structure <br/>
7. Tutorial <br/>
8. Environment properties <br/>
9. Tools <br/>
10. Author

---
### 1. Version
| Date | Version | Author | Changelog |
| --- | --- | --- | --- |
| 2022-01-31 | 1.0.0 | Murti Daryandono | Initial release |
---

### 2. Description
**web-example-basic** is a sample project that intended to help Java developers create basic web application using Java
based technologies based on MVC (Model View Controller) concept.
In this sample project, some feature will be provided, such as :
- Page templating
- Read environment properties
- Connection to back end REST services
- Service class based on business logic
- Controller class to handle request and response that comply with REST format (GET, DELETE, POST, PUT, PATCH)
- Test REST service
---

### 3. Technology stack
- Blade : Java web framework (here are [blade link](https://github.com/lets-blade/blade) & [baeldung link](https://www.baeldung.com/blade))
- Gson : JSON manipulation tools from Google ([Gson link](https://github.com/google/gson))
- Jetbrick : Java page templating ([Jetbrick link](https://github.com/lets-blade/blade-demos/tree/master/blade-template))
- SL4J : Java logging framework
- Project Lombok : Java getter & setter auto generation ([Project Lombok link](https://projectlombok.org/))
- JUnit : Java unit test framework
- Hibiki : HTML framework without JS ([Hibiki link](https://github.com/dashborg/hibiki))
- Clay : CSS framework implementing Lexicon design ([Clay link](https://clayui.com/))
---

### 4. Architecture

```mermaid
graph TD;
A[Web browser] --> B[Blade - Web framework];
B --> A;
B --> C[Netty - HTTP server];
C --> B;
B --> D[Jetbrick - Page template];
D --> B;
D --> E[Hibiki - HTML & Clay - CSS];
E --> D;
C --> F[Java];
F --> C;
B --> G[SL4J - Logging];
```
---

### 5. Sequence diagram

---

### 6. Project structure
```
project : web-example-basic
+-- pom.xml
+-- README.md
+-- README.img
|   +-- setup_maven_1.png
|   +-- setup_maven_2.png
+-- src
|   +-- main
|       +-- java
|           +-- id
|               +-- daryandono
|                   +-- web
|                       +-- Application.java
|                       +-- core
|                           +-- Bootstrap.java
|                       +-- module
|                           +-- example
|                               +-- IndexController.java
|                               +-- IndexService.java
|       +-- resources
|           +-- application.properties
|           +-- application-stg.properties
|           +-- application-prd.properties
|           +-- static
|               +-- css
|                   +-- atlass.css
|               +-- img
|                   +-- icons.svg                    
|   +-- test
|       +-- java
|           +-- id
|               +-- daryandono
|                   +-- web
|                       +-- test
```

---

### 7. Tutorial

---

### 8. Environment properties
| Environment | File properties | 
| --- | --- |
| Development | application.properties | 
| Staging | application-stg.properties | 
| Production | application-prd.properties | 

Contents of environment properties are :

```properties
# server configuration
server.port=[port value where your application will run]

# application configuration
mvc.statics=[path to static directory]
mvc.statics.show-list=[true if you want to be show via url]
```

---

### 9. Tools
- [Java 8]() as main language
- [Maven]() as dependency manager
- [IntelliJ]() as Java IDE (Integrated Development Environemnt)
- [Mermaid]() as markdown plugin for diagram
---

### 10. Author
> name : Murti Daryandono <br/>
email : murti.daryandono@gmail.com <br/>
twitter : murti_d <br/>
blog : https://daryandono.id