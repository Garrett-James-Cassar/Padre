# Evomaster

## Context
Automatic generation  of black box and white box tests based on the open API documentation

## Related
[Evo master](https://github.com/EMResearch/EvoMaster/tree/master/docs)

## Status
Rejected

## Review

### Black box testing

#### Positives
- Black box testing was actually really easy to set up, can be done quite easily

#### Negatives
- The Naming of the methods and variables come out wrongly as it seemly using the bytecode to generate the tests
- The tests that are generated are fine but aren't particularly complicated to write yourself and they aren't very flexible
- it's not really clear how the preconditions are set up 

### Conclusion 
My initial thoughts on this are that although it's a cool idea, the lack of good naming conventions and inflexibility damage it. 
It might be good for a one and done for a new project that doesn't have any high level tests, or taking over an  
old crappy project that you're taking over with no tests at this level. Having said that these tests aren't usually particularly clever in the first place  
and I think these can be done quite simply by writing one and doing copy and pasting and changing a few bits.  

Having gone through and renaming all the variables that were badly named doesn't feel his actually results in a time saving,  
just a fustration and on top of that, it can lead to a lazy unthinking testing process. 