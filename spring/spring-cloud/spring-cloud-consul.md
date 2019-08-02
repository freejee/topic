# Spring Cloud OpenFeign

+ [Overview](#overview)
    + [Features](#features)
    + [Getting Started](#quick-start)
    + [Quick start](#quick-start-1)
+ [Learn](#learn)
    + [Documentation](#documentation)
+ [Samples](#samples)
    + [A few examples to try out](#a-few-examples-to-try-out)

----------------------------------------------------------------------------------------------------

## Overview

Spring Cloud Consul provides [Consul](https://consul.io/) integrations for Spring Boot apps through autoconfiguration and binding to the Spring Environment and other Spring programming model idioms.

With a few simple annotations you can quickly enable and configure the common patterns inside your application and build large distributed systems with Hashicorp’s Consul.

The patterns provided include Service Discovery, Distributed Configuration and Control Bus.

### Features

Spring Cloud Consul features:

+ **`Service Discovery`**:
  instances can be registered with the Consul agent and clients can discover the instances using Spring-managed beans

+ **`Supports Ribbon`**:
  the client side load-balancer via Spring Cloud Netflix

+ **`Supports Zuul`**:
  a dynamic router and filter via Spring Cloud Netflix

+ **`Distributed Configuration`**:
  using the Consul Key/Value store

+ **`Control Bus`**:
  Distributed control events using Consul Events

### Quick Start

As long as Spring Cloud Consul and the Consul API are on the classpath any Spring Boot application with **`@EnableDiscoveryClient`** will try to contact a Consul agent on **`localhost:8500`** (the default values of **`spring.cloud.consul.host`** and **`spring.cloud.consul.port`** respectively):

``` java
@Configuration
@EnableAutoConfiguration
@EnableDiscoveryClient
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

A local Consul agent must be running.

See the [Consul agent documentation](https://consul.io/docs/agent/basics.html) on how to run an agent.

### Quick start

Bootstrap your application with [Spring Initializr](https://start.spring.io/).

## Learn

### Documentation

Each **`Spring project`** has its own; it explains in great details how you can use **`project features`** and what you can achieve with them.

 Release Version                    | Reference Doc                                                                                    | API Doc
------------------------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------
 2.2.0 M1 **`PRE`** **`CURRENT`**   | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/2.2.0.M1/)      | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/2.2.0.M1/)
 2.2.0 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-consul/spring-cloud-consul.html)           | [API Doc.](https://cloud.spring.io/spring-cloud-consul/spring-cloud-consul.html)
 2.1.3 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-consul/2.1.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-consul/2.1.x/)
 2.1.2 **`CURRENT`** **`GA`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/2.1.2.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/2.1.2.RELEASE/)
 2.0.4 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-consul/2.0.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-consul/2.0.x/)
 2.0.3 **`CURRENT`** **`GA`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/2.0.3.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/2.0.3.RELEASE/)
 1.3.7 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-consul/1.3.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-consul/1.3.x/)
 1.3.6 **`CURRENT`** **`GA`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/1.3.6.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/1.3.6.RELEASE/)
 1.2.3 **`GA`**                     | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/1.2.3.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-consul/1.2.3.RELEASE/)

## Samples

### A few examples to try out

+ [Consul Sample](https://github.com/spring-cloud/spring-cloud-consul/tree/master/spring-cloud-consul-sample)


