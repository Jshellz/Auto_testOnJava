## 🎭 Java Playwright Page Object Model (POM) Framework
A robust, scalable, and maintainable test automation framework built with Java, Playwright, and JUnit 5, implementing the Page Object Model (POM) design pattern.
Table of Contents

    Features
    Prerequisites
    Installation
    Project Structure
    Usage
    Running Tests
    Configuration

Features

    Page Object Model (POM): Separates page logic from test logic for better maintainability.
    Component-Based Design: Reusable UI components.
    JUnit 5 Integration: Leverages JUnit 5 lifecycle methods, extensions, and assertions.
    Auto-Waiting: Built-in Playwright auto-waiting mechanisms reduce flaky tests.
    HTML Reports: Generates detailed HTML test reports via Allure or ExtentReports.
    Parallel Execution: Support for parallel test execution.
    Cross-Browser Testing: Easy configuration for different browsers.

Prerequisites

    Java 11+ (JDK 11 or higher)
    Maven 3.6+ or Gradle 7+
    IDE (IntelliJ IDEA, Eclipse, or VS Code)

Installation

    Clone the repository:

git clone <your-repo-url>
cd <your-project-folder>

    Build the project:

Using Maven:
mvn clean install

Using Gradle:
gradle build

    Install Playwright browsers:

mvn exec:java -Dexec.mainClass="com.microsoft.playwright.CLI" -Dexec.args="install"

    or

gradle playwrightInstall

    Project Structure

project/
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/
│   │           └── example/
│   │               ├── pages/
│   │               │   ├── LoginPage.java
│   │               
│   └── test/
│       └── java/
│           └── com/
│               └── example/
│                   ├── tests/
│                   │   └── LoginTest.java
├── pom.xml (or build.gradle)
└── README.md

    Running Tests

    Run all tests

mvn test

    or
gradle test

    Run with specific browser:
mvn test -Dbrowser=firefox

    Run specific test file
mvn test -Dtest=LoginTest

    