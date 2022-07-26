# Java Project Setup for JPA

## Learning Goals

- Set up a new project.
- Add required dependencies for accessing H2 database and using JPA.

## Introduction

We will be creating a new Maven project in this lesson and adding the
dependencies for using JPA to interact with the H2 database.

## Create a New Project.

1. Open IntelliJ and click on “Create a New Project”
2. Name the project “jpa-example”.
3. Choose “Maven” for the “Build system” option.
4. Choose “11” for the “JDK” version.
5. Click on “Create”.

![IntelliJ new project creation screen](https://curriculum-content.s3.amazonaws.com/java-spring-1/intellij-new-project-screen.png)

## Add Dependencies

We need to add two dependencies to our project. Open up the `pom.xml` file in
the project and add these dependencies:

```xml
<dependencies>
    <dependency>
        <groupId>org.hibernate</groupId>
        <artifactId>hibernate-entitymanager</artifactId>
        <version>5.6.8.Final</version>
    </dependency>
    <dependency>
        <groupId>com.h2database</groupId>
        <artifactId>h2</artifactId>
        <version>2.1.212</version>
        <scope>compile</scope>
    </dependency>
</dependencies>
```

The `hibernate-entitymanager` provides both the JPA interface and a concrete
implementation of the classes required to interact with the H2 database.

The `h2` dependency is the database specific driver required to communicate with
the database. If you want to switch databases, you have to change this
dependency to the new database driver.

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
communicate with the H2 database from our Java app.
