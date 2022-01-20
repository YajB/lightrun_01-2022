



lightrun project notes: 

## Notes, comments, questions

### Product summary
Lightrun: Developer-centric observability platform
Configure the Lightrun agent component to add Lightrun actions at run time.
Add your logs, metrics, and traces.
Gain on-demand observability in real-time when you run your application code, without the need for hotfixes, restarts, or redeployment.
 
## Lightrun tags

Task: Use markdown to author a topic on Lightrun tag use cases. 

A Lightrun agent can be launched with one or more tags. 

Use tags to group agents together into relevant categories. 
Default tag title: Production.
 
Tags are used to:
* Label agents for filtering via the Integrated Development Environment (IDE) or Command Line Interface CLI)
* Add a Lightrun action to multiple agents that share the same tag
* Ensure that the Lightrun action is persistent for short-lived agents
For example, the use case of an agent launched on an AWS Lambda function
 
### Actions
 
This topic defines the persistence of actions added to agents and tags.

|Applied to| Action persistence|
|--|--|
|Agents| The action is deleted after the agent disconnects from the Lightrun server|
|Tags| Actions applied to tags are persistent|
 
 
