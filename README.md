# Java Project Setup for JPA

## Learning Goals

- Set up a new Maven Java project for JPA.
- Add required dependencies for accessing a PostgreSQL database using Hibernate.


## Introduction 

We will be creating a new Maven project in this lesson and adding the
dependencies for using JPA to interact with a PostgreSQL database.

## CODE ALONG - Create a New Project.

1. Open IntelliJ and click on “Create a New Project”
2. Name the project “jpa-example”.
3. Choose “Maven” for the “Build system” option.
4. Choose “11” for the “JDK” version.
5. Do not check "Add sample code".
6. Click on “Create”.

![IntelliJ new project creation screen](https://curriculum-content.s3.amazonaws.com/java-spring-1/intellij-new-project-screen.png)

## Add Dependencies

Open up the `pom.xml` file in the project and
add dependencies for PostgreSQL and Hibernate:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>org.example</groupId>
    <artifactId>jpa-example</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>11</maven.compiler.source>
        <maven.compiler.target>11</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>
    
    <!-- Add the following dependencies for Hibernate and PostgreSQL -->
    <dependencies>
        <dependency>
            <groupId>org.postgresql</groupId>
            <artifactId>postgresql</artifactId>
            <version>42.5.0</version>
        </dependency>
        <dependency>
            <groupId>org.hibernate</groupId>
            <artifactId>hibernate-entitymanager</artifactId>
            <version>5.6.8.Final</version>
        </dependency>
    </dependencies>

</project>
```

Remember to press the "Load Maven Changes" icon that appears in `pom.xml`:

![reload maven icon](https://curriculum-content.s3.amazonaws.com/6036/jpa-project-setup/reloadmaven.png)


The `postgresql` dependency is the database specific driver required to communicate with
the database. If you want to use a different database, you have to change this
dependency to the new database driver.

The `hibernate-entitymanager` provides both the JPA interface and a concrete
implementation of the classes required to interact with the PostgreSQL database.


## Add JpaMain Class

1. Create a package in the “java” folder called “org.example”.
2. Create a `JpaMain.java` file in the “org.example” package.
3. Add the following to the file:

```java
package org.example;

public class JpaMain {
    public static void main(String[] args) {

    }
}
```

## Conclusion

We have created a new Maven project and added two dependencies required to
use Hibernate to communicate with the PostgreSQL database from our Java app.
