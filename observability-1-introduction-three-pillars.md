# Three pillars of observability

## Background
The three pillars of observability are a mean of establishing a consistent approach for **_tracing_** **_metrics_** and **_logging_**

## Proposal
To establish an agreed set of standards for tracing, logging and metrics to be applied consistently across all applications in the group

## Problems trying to solve
**Logging**  
It is a non-controversial statement that logging is essential to identifying and diagnosing key issues in
production support and the development lifecycle. Logging standards should be in place in order to truely get the most
information out of logging events as possible. This should cover the following topics.

1. What kind of events should always be logged  
   [Observability - Logging - Interceptors](observability-logging-intrumentation.md)
   [//]: # ([Observability - Logging - AOP]&#40;observability-logging-aop.md&#41;  )

2. What kind of information should always be logged  
   [Observability - Logging - Structured Logging](observability-logging-structured-logging.md)

**Tracing**:  
Logging is essential for tracking events that happen within a set of microservices. When working with
several services that talk to each other in sequence. It is important to understand
- The full request lifecycle
- The time it takes to complete different sections of the full request cycle

This can be achieved by chaining related logs across bounded contexts with a tracing id and exporting the metrics to
an external metrics logger.

[Observability - Tracing](observability-tracing.md)

**Metrics**:  
Logging gives great information about what's happening within your app, however it's not perfect. Logs aren't retained 
forever and even when they are you need to rely on external teams to maintain the infrastructure and services that 
hold and host these logs. By Leveraging a metrics library you can retain a persistent record on all the useful metrics 
about your apps to help inform on things such as, which endpoints can be deprecated, failed callbacks and general 
failure metrics. 

[Observability - Metrics](observability-metrics.md)  


### Decision
We agree to adhere to logging standards in the linked documents and apply them consistently accross every service within our domain

### Status
On-going

### Consequences 
It's been fucking great
