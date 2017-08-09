# docker-gradle-demo

This project is used to demo how to migrate our functional tests from running locally to runnning in docker containers

There are two key gradle plugins that are used to accomplish this.

## Transmode Docker Gradle Plugin
We use this plugin to build a new docker image using our newly built jar.
https://github.com/Transmode/gradle-docker

## Avast Docker Compose Gradle Plugin
This plugin is used to orchestrate the running of the docker containers needed to functionally test the application.
https://github.com/avast/docker-compose-gradle-plugin

## Project Technologies
### App
* Spring Boot
* Jersey
* Cassandra

### Functional Tests
* Cucumber JVM
* Guice
* Cassandra
* Apache Http Client

## How To Run
### Package app as docker image
```./gradlew app:buildDocker```

### Package app and run functional tests
```./gradlew cle app:buildDocker ft:test```
