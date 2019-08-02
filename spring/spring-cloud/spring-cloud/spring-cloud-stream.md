# Spring Cloud Stream

+ [Overview](#overview)
    + [Binder Implementations](#binder-implementations)
    + [Quick start](#quick-start)
+ [Learn](#learn)
    + [Documentation](#documentation)
+ [Samples](#samples)
    + [A few examples to try out](#a-few-examples-to-try-out)

----------------------------------------------------------------------------------------------------

## Overview

Spring Cloud Stream is a framework for building highly scalable event-driven microservices connected with shared messaging systems.

The framework provides flexible programming model built on already established and familiar Spring idioms and best practices, including support for persistent pub/sub semantics, consumer groups, and stateful partitions.

### Binder Implementations

Spring Cloud Stream supports a variety of binder implementations and the following table includes the link to the GitHub projects.

+ [RabbitMQ](https://github.com/spring-cloud/spring-cloud-stream-binder-rabbit)

+ [Apache Kafka](https://github.com/spring-cloud/spring-cloud-stream-binder-kafka)

+ [Kafka Streams](https://github.com/spring-cloud/spring-cloud-stream-binder-kafka/tree/master/spring-cloud-stream-binder-kafka-streams)

+ [Amazon Kinesis](https://github.com/spring-cloud/spring-cloud-stream-binder-aws-kinesis)

+ [Google PubSub (partner maintained)](https://github.com/spring-cloud/spring-cloud-gcp/tree/master/spring-cloud-gcp-pubsub-stream-binder)

+ [Solace PubSub+ (partner maintained)](https://github.com/SolaceProducts/spring-cloud-stream-binder-solace)

+ [Azure Event Hubs (partner maintained)](https://github.com/microsoft/spring-cloud-azure/tree/master/spring-cloud-azure-stream-binder/spring-cloud-azure-eventhubs-stream-binder)

The core building blocks of Spring Cloud Stream are:

+ **`Destination Binders`**:
  Components responsible to provide integration with the external messaging systems.

+ **`Destination Bindings`**:
  Bridge between the external messaging systems and application provided Producers and Consumers of messages (created by the Destination Binders).

+ **`Message`**:
  The canonical data structure used by producers and consumers to communicate with Destination Binders (and thus other applications via external messaging systems).

### Quick start

Bootstrap your application with [Spring Initializr](https://start.spring.io/).

## Learn

### Documentation

Each **`Spring project`** has its own; it explains in great details how you can use **`project features`** and what you can achieve with them.

 Release Version                      | Reference Doc                                                                                                            | API Doc
--------------------------------------|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------
 Horsham M2 **`PRE`** **`CURRENT`**   | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-stream/3.0.0.M2/home.html)                     | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-stream/3.0.0.M2/home.html)
 Germantown **`GA`** **`CURRENT`**    | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-stream/2.2.0.RELEASE/home.html)                | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-stream/2.2.0.RELEASE/home.html)
 Fishtown SR3 **`GA`**                | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-stream/2.1.3.RELEASE/)                         | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-stream/2.1.3.RELEASE)
 Fishtown **`SNAPSHOT`**              | [Reference Doc.](https://docs.spring.io/spring-cloud-stream/docs/Fishtown.BUILD-SNAPSHOT/reference/htmlsingle/)          | [API Doc.](https://docs.spring.io/spring-cloud-stream/docs/Fishtown.BUILD-SNAPSHOT/api/)
 Elmhurst SR3 **`GA`**                | [Reference Doc.](https://docs.spring.io/spring-cloud-stream/docs/Elmhurst.SR3/reference/htmlsingle/)                     | [API Doc.](https://docs.spring.io/spring-cloud-stream/docs/Elmhurst.SR3/api/)
 Ditmars SR5 **`GA`**                 | [Reference Doc.](https://docs.spring.io/spring-cloud-stream/docs/Ditmars.SR5/reference/htmlsingle/)                      | [API Doc.](https://docs.spring.io/spring-cloud-stream/docs/Ditmars.SR5/api/)
 Ditmars **`SNAPSHOT`**               | [Reference Doc.](https://docs.spring.io/spring-cloud-stream/docs/Ditmars.BUILD-SNAPSHOT/reference/htmlsingle/)           | [API Doc.](https://docs.spring.io/spring-cloud-stream/docs/Ditmars.BUILD-SNAPSHOT/api/)
 Chelsea SR2 **`GA`**                 | [Reference Doc.](https://docs.spring.io/spring-cloud-stream/docs/Chelsea.SR2/reference/htmlsingle/index.html)            | [API Doc.](https://docs.spring.io/spring-cloud-stream/docs/Chelsea.SR2/api/)
 Chelsea **`SNAPSHOT`**               | [Reference Doc.](https://docs.spring.io/spring-cloud-stream/docs/Chelsea.BUILD-SNAPSHOT/reference/htmlsingle/index.html) | [API Doc.](https://docs.spring.io/spring-cloud-stream/docs/Chelsea.BUILD-SNAPSHOT/api/)
 Brooklyn SR3 **`GA`**                | [Reference Doc.](https://docs.spring.io/spring-cloud-stream/docs/Brooklyn.SR3/reference/htmlsingle/)                     | [API Doc.](https://docs.spring.io/spring-cloud-stream/docs/Brooklyn.SR3/api/)

## Samples

### A few examples to try out

+ [Samples](https://github.com/spring-cloud/spring-cloud-stream-samples/):
  Spring Cloud Stream sample applications


