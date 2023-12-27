# Open API 3

## Context
Consideration of the usage of Open API 3 in General

## Related
[Open API 3 tools](open-api3-tools.md)

## Status
Trialing

## Positive Consequences


### Planning  
Having written the open API 3 specification I found that my ideas about what the application does and how it  should work 
crystallizing a lot more clearly than before. There seems a clear benefit to describing the entry points and how it should 
work under the hood. While there was no clear design  document created fo this application diagrams were create about the 
way it should work. While those helped To get an initial idea, the low level and on the ground documentation of 
"how will the interactions take place" definitely helped me to think about it in a different way and had me potentially rewriting code already. 

## Negative Consequences

### Code Cleanliness
While I'm a fan of the documentation and planning of Open API 3 so far, how cluttered it made the resources did make me a bit grumpy.

### Resolution 
Consider using Yaml format instead. 

#### Update
I decided to give up on using yaml  instead  of annotations because the setup seemed quite Esoteric and you can access 
an automatically generated yaml file at http://localhost:8080/v3/api-docs.yaml. 

I will have to live with the messiness of the spring fox.