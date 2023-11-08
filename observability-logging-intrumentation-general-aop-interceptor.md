# Logging Instrumentation Connectors

## Context
[Logging Instrumentation](observability-logging-intrumentation.md)

## Problem
Logging the events in question

## Solution
1. Follow the package structure defined in [Package Structure](code-style-package-structure.md)
2. Import the library defined here: 

The library instruments the codebase by instrumenting any method in a connector class and logging the incoming request
(method parameters) and outgoing response (return value)

```agsl


```


## Decision
[Proposed, Accepted, Pending, Deprecated, Superseded]

## Related
Alternative [Spring HTTP Interceptor](observability-logging-intrumentation-spring-http-interceptor.md)  
