---
title: How to use Testcontainers with integration tests
---

## How to use Testcontainers with integration tests

![](img/logo.png)

# Testing

One of the key tasks in software development is testing.

# Test Levels

According to the test levels pyramid of Mike Cohn; there are 3 main levels:

1. Unit Test
2. Integration Test
3. UI Test

# Test pyramid

![Figure 1. Test pyramid.](img/test-pyramid.png)
[https://martinfowler.com/bliki/TestPyramid.html](https://martinfowler.com/bliki/TestPyramid.html)

# Integration test
Unit tests as a basis, and integration tests to verify interaction with external components outside the business logic.

# Testcontainers  
Testcontainers is a java library that we can use to run different testing frameworks (as JUnit or Spock) with docker containers. Docker as a developer tool, allows us to create easily environments with all its dependencies; they are light and run quickly and, also are portable.

# Not only Java

There are implementations for Go, dotNet, Python, Node, and Rust.

# Modules

* Databases (SQL, NoSQL)
* Cloud (AWS using localstack, Azure, GCloud)
* Kafka, MockServer, Solr, Vault...
* GenericContainers 

# Requirements for common JVM applications

* [Docker](https://www.testcontainers.org/supported_docker_environment/)
* [junit-jupiter](https://search.maven.org/search?q=a:junit-jupiter%20AND%20g:org.testcontainers) for JUnit 5.

# @nnotations

* [`@Testcontainers`](https://javadoc.io/doc/org.testcontainers/junit-jupiter/latest/org/testcontainers/junit/jupiter/Testcontainers.html): This annotation handles automatically the container’s lifecycle. It is in charge of start-up and closed-up every container in our tests.

* [`@Container`](https://javadoc.io/doc/org.testcontainers/junit-jupiter/latest/org/testcontainers/junit/jupiter/Container.html): Marks containers to be managed by the Testcontainers extension.

# Demo time!

# Conclusions 1/2

* Working with Testcontainers doesn't require a lot of setup.

* The [`withTmpFs`](https://javadoc.io/static/org.testcontainers/testcontainers/1.15.0-rc2/org/testcontainers/containers/GenericContainer.html#withTmpFs-java.util.Map -) option allows us to map the container volume to our host memory.

* If we want to speed up our integration tests we can declare containers as static fields to share between tests. In our case, our test run on an average bellow to 150ms.

# Conclusions 2/2

* Testcontainers provides the benefit of 100% database compatibility (since it runs a real database inside a container).

* The database always starts in a known state, without contamination between test runs.

# More info

* [https://testcontainers.org](https://testcontainers.org)

* [@testcontainers](https://twitter.com/testcontainers)

# Juan Moreno

* Blog: [https://proitcsolution.com.ve](https://proitcsolution.com.ve)

* Twitter: [@JuanMorenoDev](https://twitter.com/JuanMorenoDev)

* Presentation link: [https://bit.ly/testcontainers-careerday-2023](https://bit.ly/testcontainers-careerday-2023) 

![Figure 2. QR](img/qr.png)