# Spring Cloud OpenFeign

+ [Overview](#overview)
    + [Features](#features)
    + [Getting Started](#getting-started)
    + [Quick start](#quick-start)
+ [Learn](#learn)
    + [Documentation](#documentation)
+ [Samples](#samples)
    + [A few examples to try out](#a-few-examples-to-try-out)

----------------------------------------------------------------------------------------------------

## Overview

This project provides [OpenFeign](https://github.com/OpenFeign/feign) integrations for Spring Boot apps through autoconfiguration and binding to the Spring Environment and other Spring programming model idioms.

### Features

+ **`Declarative REST Client`**:
  Feign creates a dynamic implementation of an interface decorated with JAX-RS or Spring MVC annotations

### Getting Started

``` java
@SpringBootApplication
@EnableFeignClients
public class WebApplication {

    public static void main(String[] args) {
        SpringApplication.run(WebApplication.class, args);
    }

    @FeignClient("name")
    static interface NameService {
        @RequestMapping("/")
        public String getName();
    }

}
```

### Quick start

Bootstrap your application with [Spring Initializr](https://start.spring.io/).

## Learn

### Documentation

Each **`Spring project`** has its own; it explains in great details how you can use **`project features`** and what you can achieve with them.

 Release Version                    | Reference Doc                                                                                       | API Doc
:-----------------------------------|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------
 2.2.0 M1 **`PRE`** **`CURRENT`**   | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-openfeign/2.2.0.M1/)      | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-openfeign/2.2.0.M1/)
 2.2.0 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-openfeign/spring-cloud-openfeign.html)        | [API Doc.](https://cloud.spring.io/spring-cloud-openfeign/spring-cloud-openfeign.html)
 2.1.3 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-openfeign/2.1.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-openfeign/2.1.x/)
 2.1.2 **`GA`** **`CURRENT`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-openfeign/2.1.2.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-openfeign/2.1.2.RELEASE/)
 2.0.5 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-openfeign/2.0.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-openfeign/2.0.x/)
 2.0.4 **`GA`** **`CURRENT`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-openfeign/2.0.4.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-openfeign/2.0.4.RELEASE/)

## Samples

### A few examples to try out

+ [Feign Using Eureka](https://github.com/spring-cloud-samples/feign-eureka)


