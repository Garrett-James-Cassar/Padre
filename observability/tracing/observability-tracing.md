# Tracing

## Context
Linking logs across different spans and contexts as well as measuring latency of API calls and components of API calls.

## Solution
1. Add trace IDs 
2. Attach trace IDs to the logs
3. Export the logs

## Related

## Decision
Accepted

## Status

## Conclusions
- I think it's pretty silly not to do tracing. It's pretty fast to set up and very useful.
- The downside to exporting the logs is that it requires a tracing server. So it requires a bit of buy in if your organisation is shitty. 
- There isn't really a downside to generating the traces themselves and attaching them to the logs. 
