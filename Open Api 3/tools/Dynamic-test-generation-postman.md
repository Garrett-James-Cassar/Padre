# Dynamic Test generation - POstman

## Context
Automatic generation of black box and white box tests based on the open API documentation

## Related
[Postman](https://www.postman.com/postman-galaxy/dynamically-generate-tests-from-open-api-specs/)

## Status
Trailing

## Review
- So far this looks really promising, postman has a chatbot that just generates javascript tests automatically using your open API definition. 
- This looks like it can generate multiple types of tests like API tests, performance tests and  contract tests - but still testing that.
- This also looks like it has automatic CI integrations so could be really good for automation.
- Only generates tests when the response type is JSON or XML, this is fine.

#### Positives
- The tests actually look pretty good
- Javascript is actually pretty fast

#### Negatives
- Having a difficult time generating all types of tests. There seems to be an error that says that it can only generate tests with a json response. Even though they are all json.
- Generating these tests don't look to be free :E

### Conclusion 
