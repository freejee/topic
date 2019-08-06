# Spring Cloud for Amazon Web Services

+ [Overview](#overview)
    + [Features](#features)
        + [Annotation-based SQS Queue Listener](#annotation-based-sqs-queue-listener)
        + [Annotation-based SNS Listener](#annotation-based-sns-listener)
        + [Messaging Templates](#messaging-templates)
    + [Quick start](#quick-start)
+ [Learn](#learn)
    + [Documentation](#documentation)
+ [Samples](#samples)
    + [A few examples to try out](#a-few-examples-to-try-out)

----------------------------------------------------------------------------------------------------

## Overview

Spring Cloud for Amazon Web Services, part of the Spring Cloud umbrella project, eases the integration with hosted Amazon Web Services.

It offers a convenient way to interact with AWS provided services using well-known Spring idioms and APIs, such as the messaging or caching API.

Developers can build their application around the hosted services without having to care about infrastructure or maintenance.

### Features

+ Spring Messaging API implementation for [SQS](https://aws.amazon.com/sqs/).

+ Spring Cache API implementation for [ElastiCache](https://aws.amazon.com/elasticache/).

+ Annotation-based mapping of [SNS](https://aws.amazon.com/sns/) endpoints (HTTP).

+ Access the resources by their logical name defined in a [CloudFormation](https://aws.amazon.com/cloudformation/) stack.

+ Automatic JDBC **`DataSource`** creation based on the logical name of an [RDS](https://aws.amazon.com/rds/) instance.

+ Ant-style path matching **`ResourceLoader`** for [S3](https://aws.amazon.com/s3/) buckets.

#### Annotation-based SQS Queue Listener

``` java
@MessageMapping("logicalQueueName")
private void receiveMessage(Person person, @Header("SenderId") String senderId) {
    // ...
}
```

#### Annotation-based SNS Listener

``` java
@Controller
@RequestMapping("/sns/receive")
public class SnsEndpointController {

@NotificationMessageMapping
public void receiveNotification(@NotificationMessage String message, @NotificationSubject String subject) {
    // ...
}

@NotificationSubscriptionMapping
public void confirmSubscription(NotificationStatus notificationStatus) {
    notificationStatus.confirmSubscription();
}
```

#### Messaging Templates

``` java
snsTemplate.sendNotification("SnsTopic", "message", "subject");
sqsTemplate.convertAndSend("Queue", new Person("John", "Doe"));
```

### Quick start

Bootstrap your application with [Spring Initializr](https://start.spring.io/).

## Learn

### Documentation

Each **`Spring project`** has its own; it explains in great details how you can use **`project features`** and what you can achieve with them.

 Release Version                    | Reference Doc                                                                                 | API Doc
:-----------------------------------|:----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------
 2.2.0 M1 **`PRE`** **`CURRENT`**   | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/2.2.0.M1/)      | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/2.2.0.M1/)
 2.2.0 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-aws/spring-cloud-aws.html)              | [API Doc.](https://cloud.spring.io/spring-cloud-aws/spring-cloud-aws.html)
 2.1.3 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-aws/2.1.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-aws/2.1.x/)
 2.1.2 **`GA`** **`CURRENT`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/2.1.2.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/2.1.2.RELEASE/)
 2.0.4 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-aws/2.0.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-aws/2.0.x/)
 2.0.3 **`GA`** **`CURRENT`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/2.0.3.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/2.0.3.RELEASE/)
 1.2.5 **`SNAPSHOT`** **`CURRENT`** | [Reference Doc.](https://cloud.spring.io/spring-cloud-aws/1.2.x/)                             | [API Doc.](https://cloud.spring.io/spring-cloud-aws/1.2.x/)
 1.2.4 **`GA`** **`CURRENT`**       | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/1.2.4.RELEASE/) | [API Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/1.2.4.RELEASE/)
 1.1.4 **`GA`**                     | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/1.1.4.RELEASE/) | [API Doc.](https://github.com/spring-cloud/spring-cloud-aws)
 1.0.4 **`GA`**                     | [Reference Doc.](https://cloud.spring.io/spring-cloud-static/spring-cloud-aws/1.0.4.RELEASE/) | [API Doc.](https://github.com/spring-cloud/spring-cloud-aws)

## Samples

### A few examples to try out

+ [Reference Application](https://github.com/spring-cloud-samples/aws-refapp)


