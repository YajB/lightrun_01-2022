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

## Lightrun action targets

You decide which [Lightrun actions](https://docs.lightrun.com/actions/) to add to your application code. 

Lightrun actions are always associated with a target. The target of an action can be either an agent or a [tag](#lightrun-tags). 

### Actions and agents

Actions that are associated with an agent are deleted once the agent disconnects from the Lightrun server. 

### Actions and tags

Actions that are associated with tags are persistent: Tagged actions are saved after you shut down an agent. 
Once an action is associated with a tag, it is implicitly added to the _agents_ that are also associated with that tag.

## Lightrun tags

Lightrun tags are used to group agents together into logical categories, usually based on common functionality. 

You can use tags to group your agents by region, environment, purpose, or by any criteria that are relevant for your organization. The default tag for a Lightrun agent is `Production`.


When you apply multiple tags, you can associate actions with an agent _before_ it launches, and you can apply actions to multiple applications wherever they are running. 

The agents that are associated with a specific tag also inherit the actions associated with that tag.

### Use cases for Lightrun tags

You can apply multiple tags to your Lightrun agents, then use tags to:

- **Group your agents**
  Use tags to identify your agents by region, environment, purpose, or by any criteria that are relevant for your organization. The default tag for a Lightrun agent is `Production`.
  
- **Associate actions with agents** 
  When you apply multiple tags, you can associate actions with an agent _before_ it launches, and you can apply actions to multiple applications regardless of where they are running. 

  The agents that are associated with a specific tag also inherit the actions associated with that tag.


- **Label and filter agents in your code**
  Refine which agents are displayed in your integated development environment (IDE) or command line interface (CLI).

- **Consistently apply a Lightrun action to a group of short-lived agents** 
    
  **Example** <br>
    If you use AWS Lambda function services to manage runtime costs, when you have code that runs only for specific triggering events, you can use tags to ensure that Lightrun actions are added to your code each time those services run. 

    Associate the Lightrun actions you want to add with a tag: This ensures that the relevant Lightrun actions are added each time the services run.

    If you were to add the actions to an agent, they would be deleted each time the agent disconnected from the server.
