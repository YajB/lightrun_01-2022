# Overview of Lightrun entities

A Lightrun action is a snapshot, dynamic log, or metric that you add to specific lines within the source code for your application to capture instantaneous parameter values when your code executes.

When you add an action, a request to the agent is triggered. 
After the agent verifies the request, it adds the relevant instrumentation to the running application, without interrupting services.

## Lightrun agents

You can configure and use Lightrun agents to add specific Lightrun actions to your application, without having to apply hotfixes, restart, or redeploy any of the applications or components in your environment: The agent runs as an additional thread alongside your applications. 

The following Lightrun agents are available for your environment: 
- Java agent
- Python agent
- Node.js agent


## Lightrun tags

Lightrun tags are used to group agents together into logical categories. 
Create tags to group your agents by region, environment, or by other criteria that are relevant for your organization. 

### Lightrun action and tag properties

Actions that are added to an agent are deleted once the agent disconnects from the Lightrun server. 
In contrast to this behavior, actions that are added to tags are persistent. 

### Use cases for tags

You can apply multiple tags to your Lightrun agents, then use the tags to:
* Label and filter agents in your integated development environment (IDE) or command line interface (CLI).
* Associate Lightrun actions to a group of agents labeled with a specific tag.
* Consistently apply a Lightrun action to a group of short-lived agents. 
  
**Example** 
For your AWS Lambda function services that run code for specific triggering events, to ensure that the relevant Lightrun actions are added each time the services run, associate these actions with a tag, rather than associating the actions directly to the agents. 

If you add the actions to the agent, they're going to be deleted each time the agent disconnects from the server.

