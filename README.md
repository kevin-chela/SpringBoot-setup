# Spring Boot


## Requirements

- Java 17 JDK (Amazon Corretto version 18)
- Gradle
- IntelliJ IDEA Community Edition or any other Kotlin-compatible IDE

## Setup Instructions

1. **Generate the Project**:
    - Visit [Spring Initializr](https://start.spring.io/).
    - Set up the project as follows:
        - **Project**: Gradle Project
        - **Language**: Kotlin
        - **Spring Boot**: 3.0.0
        - **Group**: `com.example`
        - **Artifact**: `demo`
        - **Name**: `demo`
        - **Package Name**: `com.example.demo`
        - **Packaging**: Jar
        - **Java Version**: 17
    - Add the following dependencies:
        - Spring Web
        - Spring Data JDBC
        - H2 Database
    - Click `Generate` to download the project.

2. **Import the Project into IntelliJ IDEA**:
    - Extract the downloaded zip file.
    - Open IntelliJ IDEA and select `Open or Import`.
    - Navigate to the extracted project directory and select it.
    - Choose `Open as Project`.
    - IntelliJ IDEA will download the necessary dependencies.

3. **Run the Application**:
    - Open `DemoApplication.kt`.
    - Right-click and select `Run 'DemoApplication'`.
    - Alternatively, click the green play button in the top right corner.
    - The application will start on port 8080.

## Adding Topics

To add new topics or features, create new packages and classes as needed. For example:

### Creating a REST Controller

```kotlin
package com.example.demo.controller

import org.springframework.web.bind.annotation.GetMapping
import org.springframework.web.bind.annotation.RestController

@RestController
class HelloController {

    @GetMapping("/hello")
    fun sayHello(): String {
        return "Hello, World!"
    }
}


