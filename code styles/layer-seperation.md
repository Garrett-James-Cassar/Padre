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
[Arch Unit Tests for package structure](../testing/structure%20testing/package-structure.md)  
[Arch Unit Tests for tolerable reader pattern](../testing/structure%20testing/tolerable-reader.md)  
[Instrumentation](../observability/intrumentation.md)

## Decision
Accepted

## Status
Implemented and blog post almost done

## Consequences
#### 08.11.23
So far so good

#### 16.11.23 
I'm finding it a little annoying having to insert the adaptor all the time, especially when I'm doing something  
relatively straight forward.  
I'm finding this particularly annoying on the database front. When the operation is 'Get this from one repository and then  
get another thing from another repository based on the first thing' I'm finding the fact the that you need to convert    
into the entity format and convert out the result of the first thing again quite annoying. On top of that I find   
the use of companion objects to convert class types much nicer looking, both in line and at a class dependency level.  

I'm considering three things: 
1. Ease up the rule for database entities
   1. Maybe adaptor could not be part of the rule at all, and we just base the arch unit tests on Services and connector layers
   2. Maybe we put databases in it's special package and right a rull that the resource layer is not to speak to the database
   
2. Try and change the Arch unit tests so that instead of targeting adaptor classes, they target companion objects

3. Have the adaptors actually just consist of extension functions and base the rule on any function calls defined in that package.



