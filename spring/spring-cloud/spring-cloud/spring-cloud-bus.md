# Spring Cloud Bus

+ [Overview](#overview)
    + [Getting Started](#getting-started)
    + [Quick start](#quick-start)
+ [Learn](#learn)
    + [Documentation](#documentation)
+ [Samples](#samples)
    + [A few examples to try out](#a-few-examples-to-try-out)

----------------------------------------------------------------------------------------------------

## Overview

Spring Cloud Bus links nodes of a distributed system with a lightweight message broker.

This can then be used to broadcast state changes (e.g. configuration changes) or other management instructions.

The only implementation currently is with an AMQP broker as the transport, but the same basic feature set (and some more depending on the transport) is on the roadmap for other transports.

### Getting Started

As long as Spring Cloud Bus AMQP and RabbitMQ are on the classpath any Spring Boot application will try to contact a RabbitMQ server on **`localhost:5672`** (the default value of **`spring.rabbitmq.addresses`**):

``` java
@Configuration
@EnableAutoConfiguration
@RestController
public class Application {

    @RequestMapping("/")
    public String home() {
        return "Hello World";
    }

    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }

}
```

### Quick start

Bootstrap your application with [Spring Initializr](https://start.spring.io/).

## Learn

### Documentation

Each **`Spring project`** has its own; it explains in great details how you can use **`project features`** and what you can achieve with them.

 Release Version                    | Reference Doc                                                                                 | API Doc
:-----------------------------------|:----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------
 2.2.0 M1 **`PRE`** **`CURRENT`**   | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/2.2.0.M1/)      | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/2.2.0.M1/)
 2.2.0 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-bus/spring-cloud-bus.html)              | [API Doc.](https://cloud.spring.io/spring-cloud-bus/spring-cloud-bus.html)
 2.1.3 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-bus/2.1.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-bus/2.1.x/)
 2.1.2 **`GA`** **`CURRENT`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/2.1.2.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/2.1.2.RELEASE/)
 2.0.3 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-bus/2.0.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-bus/2.0.x/)
 2.0.2 **`GA`** **`CURRENT`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/2.0.2.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/2.0.2.RELEASE/)
 1.2.1 **`GA`**                     | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/1.2.1.RELEASE/) | [API Doc.](https://github.com/spring-cloud/spring-cloud-bus)
 1.1.1 **`GA`**                     | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/1.1.1.RELEASE/) | [API Doc.](https://github.com/spring-cloud/spring-cloud-bus)
 1.0.3 **`GA`**                     | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-bus/1.0.3.RELEASE/) | [API Doc.](https://github.com/spring-cloud/spring-cloud-bus)

## Samples

### A few examples to try out

+ [Bus Clients](https://github.com/spring-cloud-samples/customers-stores)


