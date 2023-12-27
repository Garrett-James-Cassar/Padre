# Spring fox

## Context
Consideration of the usage of Spring fox in order to generate openAPI 3 schema from annotations

## Status
Trialing

## Positive Consequences



## Negative Consequences
### Clunkities

- I'm still finding the openAPI annotations a bit clunky, annotations in general are quite a restrictive way of doing things, as it relies
  on a lot of reflection. This means it's sort of difficult to tell you exactly what you want.  
  For example a lot of the time you ask for an Array of potential responses, but the example will only return a single response.  
  It's difficult to add 3 different responses where the response codes are all 404. For this reason I find it's better that these parts of the api documentation
  represents internally maintained codes rather than http codes. Similarly with responses.

- Another clunkity is the constants are not represented   as  values but only the classes they represents.

- Links don't work in a way that displays properly in swagger. 
I wanted to try to use this to create a panache query for the 404 errors. 

### Code Cleanliness
While I'm a fan of the documentation and planning of Open API 3 so far, how cluttered it made the resources did make me a bit grumpy.

### Resolution
Consider using Yaml format instead.

#### Update
I decided to give up on using yaml  instead  of annotations because the setup seemed quite Esoteric and you can access
an automatically generated yaml file at http://localhost:8080/v3/api-docs.yaml.

I will have to live with the messiness of the annotations.

22-12-2023

### Conclusion
- Although I really like the concept of openAPI Swagger spring docs seems very limited and clunky. 
- It doesn't even really support all the features of the openAPI3 standard. It will do, but not wooed
