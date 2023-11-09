# AI in DevSecOps 

### Predictive  
#### Production Incident Avoidance
- Use cases
- Analyse data on production support
    - Which incidents happen most frequently
    - Which incidents do customers ask about most?
    - Which incidents cost most money

- Which JIRAs spend most time in which column?

#### Scaling 
- Need to provision DynamoDB autoscaling 

Dynamo can handle this but it takes several minutes, so you either need to waste capacity or have scaling up issues
You could have a scaling schedule which is useful, but it still causes wastage for the log ins. 
The problem is that teh schedules are very different in seasons. 

AWS Forecast is used to create a scaling schedule for the min value scale so it's scaled ahead of time  

### Generative

#### Security
GPT is quite good at doing and creating tabletop exercises. This is really useful for: 
- Refresher training
- 



Note: look up Amplify Education
Note: look up Akkio AI
Note: look up Quickbase
Note: look up Datadog
Note: K-12 curriculum
Tabletop exercises -> mock production incident
