# Lightrun entities
# Overview of Lightrun entities

A Lightrun action is a snapshot, dynamic log, or metric that you add to specific lines within the source code for your application to capture instantaneous parameter values when your code executes.

When you add an action, that triggers a request to the agent. 
After the agent verifies the request, it adds the relevant instrumentation to the application without interrupting services.


## Lightrun agents

You can configure and use Lightrun agents to add specific Lightrun actions to your application, without having to apply hotfixes, restart, or redeploy any of the applications or components in your environment: The agent runs as an additional thread alongside your applications. 

The following Lightrun agents are available for your environment: 
- Java agent
- Python agent
- Node.js agent


## Lightrun tags

Lightrun tags are used to group agents together into logical categories, usually based on common functionality. 

You can use tags to group your agents by region, environment, purpose, or by any criteria that are relevant for your organization. The default tag for a Lightrun agent is `Production`.

When you apply multiple tags, you can associate actions with an agent before it launches

### Lightrun actions and tag properties

Actions that are added to an agent are deleted once the agent disconnects from the Lightrun server. 
In contrast to this behavior, actions that are added to tags are persistent. 

### Use cases for tags

You can apply multiple tags to your Lightrun agents, then use the tags to:
* Label and filter agents in your integated development environment (IDE) or command line interface (CLI).
* Associate Lightrun actions to a group of agents labeled with a specific tag.
* Consistently apply a Lightrun action to a group of short-lived agents. 
    
    **Example** 

    If you use serverless AWS Lambda function services to manage runtime costs, for code that only runs for specific triggering events, you can use tags to ensure that Lightrun actions are added to your code each time the services run. 

    Associate the Lightrun actions you want to add with a tag: This ensures that the relevant Lightrun actions are added each time the services run.

    If you were to add the actions to an agent, they would be deleted each time the agent disconnects from the server.

