# Spring Cloud

+ [Overview](#overview)
    + [Features](#features)
    + [Main Projects](#main-projects)
    + [Release Trains](#release-trains)
    + [Talks and Videos](#talks-and-videos)
    + [Quick start](#quick-start)
+ [Learn](#learn)
    + [Documentation](#documentation)
+ [Samples](#samples)
    + [A few examples to try out](#a-few-examples-to-try-out)

----------------------------------------------------------------------------------------------------

## Overview

Spring Cloud provides tools for developers to quickly build some of the common patterns in distributed systems (e.g. configuration management, service discovery, circuit breakers, intelligent routing, micro-proxy, control bus, one-time tokens, global locks, leadership election, distributed sessions, cluster state).

Coordination of distributed systems leads to boiler plate patterns, and using Spring Cloud developers can quickly stand up services and applications that implement those patterns.

They will work well in any distributed environment, including the developer’s own laptop, bare metal data centres, and managed platforms such as Cloud Foundry.

### Features

Spring Cloud focuses on providing good out of box experience for typical use cases and extensibility mechanism to cover others.

+ Distributed/versioned configuration

+ Service registration and discovery

+ Routing

+ Service-to-service calls

+ Load balancing

+ Circuit Breakers

+ Global locks

+ Leadership election and cluster state

+ Distributed messaging

Spring Cloud takes a very declarative approach, and often you get a lot of features with just a classpath change and/or an annotation.

Example application that is a discovery client:

``` java
@SpringBootApplication
@EnableDiscoveryClient
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```

### Main Projects

+ [Spring Cloud Config](https://cloud.spring.io/spring-cloud-config):
  Centralized external configuration management backed by a git repository.
  The configuration resources map directly to Spring **`Environment`** but could be used by non-Spring applications if desired.

+ [Spring Cloud Netflix](https://cloud.spring.io/spring-cloud-netflix):
  Integration with various Netflix OSS components (Eureka, Hystrix, Zuul, Archaius, etc.).

+ [Spring Cloud Bus](https://cloud.spring.io/spring-cloud-bus):
  An event bus for linking services and service instances together with distributed messaging.
  Useful for propagating state changes across a cluster (e.g. config change events).

+ [Spring Cloud Cloudfoundry](https://cloud.spring.io/spring-cloud-cloudfoundry):
  Integrates your application with Pivotal Cloud Foundry.
  Provides a service discovery implementation and also makes it easy to implement SSO and OAuth2 protected resources.

+ [Spring Cloud Open Service Broker](https://cloud.spring.io/spring-cloud-open-service-broker):
  Provides a starting point for building a service broker that implements the Open Service Broker API.

+ [Spring Cloud Cluster](https://github.com/spring-cloud/spring-cloud-cluster):
  Leadership election and common stateful patterns with an abstraction and implementation for Zookeeper, Redis, Hazelcast, Consul.

+ [Spring Cloud Consul](https://cloud.spring.io/spring-cloud-consul):
  Service discovery and configuration management with Hashicorp Consul.

+ [Spring Cloud Security](https://cloud.spring.io/spring-cloud-security):
  Provides support for load-balanced OAuth2 rest client and authentication header relays in a Zuul proxy.

+ [Spring Cloud Sleuth](https://cloud.spring.io/spring-cloud-sleuth):
  Distributed tracing for Spring Cloud applications, compatible with Zipkin, HTrace and log-based (e.g. ELK) tracing.

+ [Spring Cloud Data Flow](https://cloud.spring.io/spring-cloud-dataflow):
  A cloud-native orchestration service for composable microservice applications on modern runtimes.
  Easy-to-use DSL, drag-and-drop GUI, and REST-APIs together simplifies the overall orchestration of microservice based data pipelines.

+ [Spring Cloud Stream](https://cloud.spring.io/spring-cloud-stream):
  A lightweight event-driven microservices framework to quickly build applications that can connect to external systems.
  Simple declarative model to send and receive messages using Apache Kafka or RabbitMQ between Spring Boot apps.

+ [Spring Cloud Stream App Starters](https://cloud.spring.io/spring-cloud-stream-app-starters):
  Spring Cloud Stream App Starters are Spring Boot based Spring Integration applications that provide integration with external systems.

+ [Spring Cloud Task](https://cloud.spring.io/spring-cloud-task):
  A short-lived microservices framework to quickly build applications that perform finite amounts of data processing.
  Simple declarative for adding both functional and non-functional features to Spring Boot apps.

+ [Spring Cloud Task App Starters](https://cloud.spring.io/spring-cloud-task-app-starters):
  Spring Cloud Task App Starters are Spring Boot applications that may be any process including Spring Batch jobs that do not run forever, and they end/stop after a finite period of data processing.

+ [Spring Cloud Zookeeper](https://cloud.spring.io/spring-cloud-zookeeper):
  Service discovery and configuration management with Apache Zookeeper.

+ [Spring Cloud AWS](https://github.com/spring-cloud/spring-cloud-aws):
  Easy integration with hosted Amazon Web Services.
  It offers a convenient way to interact with AWS provided services using well-known Spring idioms and APIs, such as the messaging or caching API.
  Developers can build their application around the hosted services without having to care about infrastructure or maintenance.

+ [Spring Cloud Connectors](https://github.com/spring-cloud/spring-cloud-connectors):
  Makes it easy for PaaS applications in a variety of platforms to connect to backend services like databases and message brokers (the project formerly known as **`Spring Cloud`**).

+ [Spring Cloud Starters](https://github.com/spring-cloud/spring-cloud-starters):
  Spring Boot-style starter projects to ease dependency management for consumers of Spring Cloud.
  (Discontinued as a project and merged with the other projects after Angel.SR2.)

+ [Spring Cloud CLI](https://github.com/spring-cloud/spring-cloud-cli):
  Spring Boot CLI plugin for creating Spring Cloud component applications quickly in Groovy

+ [Spring Cloud Contract](https://cloud.spring.io/spring-cloud-contract):
  Spring Cloud Contract is an umbrella project holding solutions that help users in successfully implementing the Consumer Driven Contracts approach.

+ [Spring Cloud Gateway](https://cloud.spring.io/spring-cloud-gateway):
  Spring Cloud Gateway is an intelligent and programmable router based on Project Reactor.

+ [Spring Cloud OpenFeign](https://cloud.spring.io/spring-cloud-openfeign):
  Spring Cloud OpenFeign provides integrations for Spring Boot apps through autoconfiguration and binding to the Spring Environment and other Spring programming model idioms.

+ [Spring Cloud Pipelines](https://cloud.spring.io/spring-cloud-pipelines):
  Spring Cloud Pipelines provides an opinionated deployment pipeline with steps to ensure that your application can be deployed in zero downtime fashion and easilly rolled back of something goes wrong.

+ [Spring Cloud Function](https://github.com/spring-cloud/spring-cloud-function):
  Spring Cloud Function promotes the implementation of business logic via functions.
  It supports a uniform programming model across serverless providers, as well as the ability to run standalone (locally or in a PaaS).

### Release Trains

Spring Cloud is an umbrella project consisting of independent projects with, in principle, different release cadences.

To manage the portfolio a BOM (Bill of Materials) is published with a curated set of dependencies on the individual project (see below).

The release trains have names, not versions, to avoid confusion with the sub-projects.

The names are an alphabetic sequence (so you can sort them chronologically) with names of London Tube stations (**`Angel`** is the first release, **`Brixton`** is the second).

When point releases of the individual projects accumulate to a critical mass, or if there is a critical bug in one of them that needs to be available to everyone, the release train will push out **`service releases`** with names ending **`.SRX`**, where **`X`** is a number.

Table 1. Release train Spring Boot compatibility

 Release Train | Boot Version
:--------------|:-------------
 Greenwich     | 2.1.x
 Finchley      | 2.0.x
 Edgware       | 1.5.x
 Dalston       | 1.5.x



Table 2. Release train contents

 Component                 | Edgware.SR6    | Finchley.SR2  | Finchley.BUILD-SNAPSHOT
:--------------------------|:---------------|:--------------|:------------------------
 spring-cloud-aws          | 1.2.4.RELEASE  | 2.0.1.RELEASE | 2.0.1.BUILD-SNAPSHOT
 spring-cloud-bus          | 1.3.4.RELEASE  | 2.0.0.RELEASE | 2.0.1.BUILD-SNAPSHOT
 spring-cloud-cli          | 1.4.1.RELEASE  | 2.0.0.RELEASE | 2.0.1.BUILD-SNAPSHOT
 spring-cloud-commons      | 1.3.6.RELEASE  | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-contract     | 1.2.7.RELEASE  | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-config       | 1.4.7.RELEASE  | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-netflix      | 1.4.7.RELEASE  | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-security     | 1.2.4.RELEASE  | 2.0.1.RELEASE | 2.0.1.BUILD-SNAPSHOT
 spring-cloud-cloudfoundry | 1.1.3.RELEASE  | 2.0.1.RELEASE | 2.0.1.BUILD-SNAPSHOT
 spring-cloud-consul       | 1.3.6.RELEASE  | 2.0.1.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-sleuth       | 1.3.6.RELEASE  | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-stream       | Ditmars.SR5    | Elmhurst.SR1  | Elmhurst.BUILD-SNAPSHOT
 spring-cloud-zookeeper    | 1.2.3.RELEASE  | 2.0.0.RELEASE | 2.0.1.BUILD-SNAPSHOT
 spring-boot               | 1.5.21.RELEASE | 2.0.6.RELEASE | 2.0.7.BUILD-SNAPSHOT
 spring-cloud-task         | 1.2.4.RELEASE  | 2.0.0.RELEASE | 2.0.1.BUILD-SNAPSHOT
 spring-cloud-vault        | 1.1.3.RELEASE  | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-gateway      | 1.0.3.RELEASE  | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-openfeign    |                | 2.0.2.RELEASE | 2.0.2.BUILD-SNAPSHOT
 spring-cloud-function     | 1.0.2.RELEASE  | 1.0.0.RELEASE | 1.0.1.BUILD-SNAPSHOT

Finchley builds and works with Spring Boot 2.0.x, and is not expected to work with Spring Boot 1.5.x.

Note: The Dalston release train will [reach end-of-life](https://spring.io/blog/2018/06/19/spring-cloud-finchley-release-is-available) in December 2018.

Edgware will follow the end-of-life cycle of Spring Boot 1.5.x.

The Dalston and Edgware release trains build on Spring Boot 1.5.x, and are not expected to work with Spring Boot 2.0.x.

> **`Note`**:
  The Camden release train was [marked end-of-life](https://spring.io/blog/2018/06/19/spring-cloud-finchley-release-is-available).
  The Camden release train builds on Spring Boot 1.4.x, but is also tested with 1.5.x.

> **`Note`**:
  The Brixton and Angel release trains were [marked end-of-life](https://spring.io/blog/2017/07/21/spring-cloud-dalston-sr2-is-available-now#end-of-life-for-angel-and-brixton-release-trains) (EOL) in July 2017.
  The Brixton release train builds on Spring Boot 1.3.x, but is also tested with 1.4.x.

The Angel release train builds on Spring Boot 1.2.x, and is incompatible in some areas with Spring Boot 1.3.x.

Brixton builds on Spring Boot 1.3.x and is similarly incompatible with 1.2.x.

Some libraries and most apps built on Angel will run fine on Brixton, but changes will be required anywhere that the OAuth2 features from spring-cloud-security 1.0.x are used (they were mostly moved to Spring Boot in 1.3.0).

Use your dependency management tools to control the version.

If you are using Maven remember that the first version declared wins, so declare the BOMs in order, with the first one usually being the most recent (e.g. if you want to use Spring Boot 1.3.6 with Brixton.RELEASE, put the Boot BOM first).

The same rule applies to Gradle if you use the Spring dependency management plugin.

> **`Note`**:
  The release train contains a **`spring-cloud-dependencies`** as well as the **`spring-cloud-starter-parent`**.
  You can use the parent as you would the **`spring-boot-starter-parent`** (if you are using Maven).
  If you only need dependency management, the **`dependencies`** version is a BOM-only version of the same thing (it just contains dependency management and no plugin declarations or direct references to Spring or Spring Boot).
  If you are using the Spring Boot parent POM, then you can use the BOM from Spring Cloud.
  The opposite is not true: using the Cloud parent makes it impossible, or at least unreliable, to also use the Boot BOM to change the version of Spring Boot and its dependencies.

### Talks and Videos

+ [Beginner's Guide To Spring Cloud](https://www.youtube.com/watch?v=aO3W-lYnw-o)

### Quick start

Bootstrap your application with [Spring Initializr](https://start.spring.io/).

## Learn

### Documentation

Each **`Spring project`** has its own; it explains in great details how you can use **`project features`** and what you can achieve with them.

 Release Version                      | Reference Doc                                                                        | API Doc
:-------------------------------------|:-------------------------------------------------------------------------------------|:----------------------------------------------------
 Greenwich SR2 **`GA`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/Greenwich.SR2/)         | [API Doc.](https://spring.io/projects/spring-cloud)
 Hoxton **`SNAPSHOT`**                | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/Hoxton.BUILD-SNAPSHOT/) | [API Doc.](https://spring.io/projects/spring-cloud)
 Greenwich **`SNAPSHOT`**             | [Reference Doc.](https://spring.io/projects/spring-cloud)                            | [API Doc.](https://spring.io/projects/spring-cloud)
 Finchley SR3 **`GA`**                | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/Finchley.SR3/)          | [API Doc.](https://spring.io/projects/spring-cloud)
 Finchley **`SNAPSHOT`**              | [Reference Doc.](https://spring.io/projects/spring-cloud)                            | [API Doc.](https://spring.io/projects/spring-cloud)
 Edgware SR6 **`GA`**                 | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/Edgware.SR6/index.html) | [API Doc.](https://spring.io/projects/spring-cloud)
 Edgware **`SNAPSHOT`**               | [Reference Doc.](https://spring.io/projects/spring-cloud)                            | [API Doc.](https://spring.io/projects/spring-cloud)
 Dalston SR5 **`GA`**                 | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/Dalston.SR5/)           | [API Doc.](https://spring.io/projects/spring-cloud)

## Samples

### A few examples to try out

+ [Config Server](https://github.com/spring-cloud-samples/configserver)

+ [Service Registry](https://github.com/spring-cloud-samples/eureka)

+ [Circuit Breaker Dashboard](https://github.com/spring-cloud-samples/hystrix-dashboard)

+ [Business Application (Customers and Stores)](https://github.com/spring-cloud-samples/customers-stores)

+ [OAuth2 Authorization Server](https://github.com/spring-cloud-samples/authserver)

+ [OAuth2 SSO Client](https://github.com/spring-cloud-samples/sso)

+ [Integration Test Samples](https://github.com/spring-cloud-samples/tests)

+ [Spring Cloud Contract Samples](https://github.com/spring-cloud-samples/spring-cloud-contract-samples)


