# Package structure

## Context
Developing any independently deployable unit that requires implementation and communication with outside resources

## Problem
Defining clear homes for code related to their structure

## Solution
Create a package structure based on the agreed layer separation (see below)

### Connectors  
All interfaces that allow the application to communicate directly with any resource that is not within the application.  
Definition to include: 
- Http Resources / Controllers
- Http Clients
- Kafka Consumers
- Kafka Producers
- Any Queue Consumers and Producers
- JDBC Connectors
- Cache repositories
- External cloud service connectors

### Data Transfer Objects (DTOs) 
All serialized representations of external messages.  
Definition to include:  
- Http Requests
- Http Responses
- Kafka Messages
- Queue Messages
- Database Entities
- Cache Entries
- External cloud service requests

### Domain classes  
All classes that are defined within the application's domain. 
- Can be used by services within the domain.  
- Can hold business logic that is true regardless of context.

### Adaptors
All classes responsible for converting 
- DTOs -> Domain classes
- Domain classes -> DTOs

### Services
Hold all methods that carry out business logic serves a singular use case. 

## Related
[Layer Separation](layer-seperation.md)  
[Package structure Arch unit tests](../testing/arch%20unit/package-structure.md)  
[Observability Instrumentation](../observability/intrumentation.md)

## Decision
[Proposed, Accepted, Pending, Deprecated, Superseded]

## Status

## Consequences
