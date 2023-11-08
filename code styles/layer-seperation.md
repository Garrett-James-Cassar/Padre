# Layer Separation

## Context
Development on a service that connects to different data source

## Problem
Muddled code with unclear responsibilities

## Solution
Separate code based on the functions within the communication with external services

### Connectors  
Things that help our application talk to anything outside the application
### Adaptors 
Things that convert the external representation of the data to the internal view of the data
### Services 
Things that carry out use cases i.e things that are true within the context of a particular context 
### Entities  
Internal representations of data that carry out central business logic i.e things that are always true without any context

_Advantages_  
This structure allows us to increase readability, reusability and inter-opability of our code. 

Structuring the code in this way also allows us to target related classes for 
1. Instrumentation tools for logging, metrics and tracing 
2. Arch unit tests for enforcing tollerable layer pattern

## Related
[Package Structure](package-structure.md)  
[Arch Unit Tests for package structure](../testing/arch unit/package-structure.md)  
[Arch Unit Tests for tolerable reader pattern](../testing/arch unit/tolerable-reader.md)  
[Instrumentation](../observability/intrumentation.md)

## Decision
[Proposed, Accepted, Pending, Deprecated, Superseded]

## Status

## Consequences
