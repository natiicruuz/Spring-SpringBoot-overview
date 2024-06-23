# Spring-SpringBoot-learning

## Set up

Spring Boot provides an embedded HP server so you can get started quickly. So it has a port for Tomcat, Jetty, and Undertow, there's no need to install a server separately.

So basically you'll have your application like `mycoolap.jar`, this JAR file will include your application code and it'll also include the embedded server.

So we'll have Tomcat that's embedded as part of your JAR file. So the nice thing about this is that
it's a self-contained unit. There's nothing else that you have to install. So there's no separate Tomcat installation you need. You actually have the application server as part of your code and you can run it independently.


So if I wanted to run my Spring Boot app, I could run it from the IDE or I could run it from the command line and it'll actually run my application and it'll also spin up the server.

## Deploying Spring boot apps


You can deploy a WAR file to an external server like Tomcat, JBoss, or WebSphere and it can work just like you would use it in the past.


## Spring Initializr

### Development Process

1. Go to `https://start.spring.io/`
   - Spring Boot: Choose the most recent version that they have here. Avoid the snapshot versions because they are alpha/beta.
   - Project: Maven
   - Language: Java
   -  Project Metadata:
        -  group ID: (example) `com.example.springboot.demo`.
        - artifact ID:  this is the actual name of the application
        - dependencies: choose the Spring Boot starters
                - Web

2. Download the zip file
3. Unzip the file
4. Import file into our IDE (VScode)

## MAVEN
Maven will go out and download the JAR files for the  projects you want for you and will automatically make those JAR files available during compile and run. So you can kind of think of Maven as like your friendly helper or your personal shopper 🛍️

### How it works?

You will have your project config file (shopping list) and Maven will read it. Then Maven will check a Maven Local Repository that resides on your computer (It's like your local cache)

If you don't have the files in your local repo, then Maven will actually go out to the internet at the Maven Central Repository, which is remote, and it'll pull those JAR files down from the Maven Central Repo on the internet.

Then it'll save versions of those files in your local repository so you can kind of build up your local cache, and then Maven will use that to build and run your application.

- It will algo download supporting dependencies.
- Maven will handle class and build path for you.
- It also provides a Standard Directory Structure

### Key Concepts
1. POM file: `pom.xml`: Config file (shopping list):

STRUCTURE:
  - Project metadata: project name, version...
  - Dependencies: List of projects we depend on. (Spring, Hibernate...)
  - Plugins for customization

2. Project Coordinates: Used to identify a project.
  - Group Id:  reverse domain name. Name of company...
  - Artifact: name of the project
  - Version: release version.
