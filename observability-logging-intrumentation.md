# Logging Instrumentation Connectors

## Context
Receiving an HTTP Request  
Sending an HTTP Request

## Problem
Logging the events in question

## Solution
1. Create a HTTP Logging interceptor that makes use of Spring Framework Logging interceptor 

_Advantages_  
- Easily implemented and well understood

_Disadvantages_
- Couples us to the Springboot framework  
- Can not be reused for other incoming and outgoing connectors (Kafka, JMS, gRPC, JDBC)

2. Create a more general logging interceptor that makes use of Aspect oriented programming instead
_Advantages_  
- Does not couple us to the springboot framework
- Can be reused for other incoming and outgoing connectors (Kafka, JMS, gRPC, JDBC)

_Disadvantages_
- Less well understood and harder to implement

## Related
[Spring HTTP Interceptor](observability-logging-intrumentation-spring-http-interceptor.md)  
[General AOP Interceptor](observability-logging-intrumentation-general-aop-interceptor.md)
