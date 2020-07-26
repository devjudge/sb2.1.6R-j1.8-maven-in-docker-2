# Spring Boot Maven

PROJECT START STEPS:

    Pre-requisites:
    1. Java must be installed
    2. Install maven module (https://maven.apache.org/install.html).

    Steps:
    1. To run this application, do the following:
        1.a. Go to the project root directory.
        1.b. Run the following commands in the terminal/command line to build the app:
            - mvn clean install
        1.c. Run the following command(s) in the terminal/command line to run the app:
            - java -jar ./target/spring-boot-in-docker.jar

    2. Go to http://localhost:8080/ in your browser to view it.

DATABASE PROPERTIES FOR SUBMISSION:

    Replace your application.properties with following to connect to MYSQL database:
    server.port=8080
    spring.datasource.url=jdbc:mysql://127.0.0.1:3306/db?useSSL=false&serverTimezone=UTC&useLegacyDatetimeCode=false
    spring.datasource.username=root
    spring.datasource.password=admin
    spring.datasource.driver-class-name=com.mysql.jdbc.Driver
    spring.datasource.testWhileIdle=true
    spring.datasource.validationQuery=SELECT 1
    spring.jpa.show-sql=true
    spring.jpa.hibernate.ddl-auto=create-drop
    spring.jpa.properties.hibernate.jdbc.lob.non_contextual_creation=true
    spring.jpa.hibernate.naming.implicit-strategy=org.hibernate.boot.model.naming.ImplicitNamingStrategyLegacyHbmImpl
    spring.jpa.hibernate.naming.physical-strategy=org.springframework.boot.orm.jpa.hibernate.SpringPhysicalNamingStrategy
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5InnoDBDialect

    Replace your application.properties with following to connect to Mongo database:
    server.port=8080
    spring.data.mongodb.authentication-database=admin
    spring.data.mongodb.username=root
    spring.data.mongodb.password=admin
    spring.data.mongodb.database=db
    spring.data.mongodb.port=27017
    spring.data.mongodb.host=localhost
