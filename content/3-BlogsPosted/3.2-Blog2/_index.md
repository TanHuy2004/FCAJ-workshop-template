---
title: "Blog 2"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---
# AgentCore Harness: From Idea to a Working AI Agent with Only Two APIs

When building an AI agent, calling a language model is rarely the hardest part. The complexity usually comes from the agent loop, tool integration, memory, session state, identity, observability, and a secure execution environment.

**Amazon Bedrock AgentCore Harness** packages these components as a managed service, allowing developers to focus on business logic instead of rebuilding orchestration and infrastructure for every agent.

---

## 1. Two Core APIs

An agent can be defined and operated through two primary APIs:

* **CreateHarness:** Defines the model, system prompt, tools, skills, memory, and execution limits.
* **InvokeHarness:** Sends a request, runs the agent, and returns its result.

Once defined, the agent can analyze a request, select appropriate tools, execute them, and respond to the application while AgentCore manages the orchestration loop.

---

## 2. What Does AgentCore Harness Manage?

Each session can run in an isolated environment with its own filesystem and shell. Harness also brings together:

* Memory and conversation state across sessions.
* Identity, access control, and Amazon CloudWatch observability.
* AgentCore Gateway for APIs, AWS Lambda, and governed tools.
* Remote MCP servers, AgentCore Browser, and AgentCore Code Interpreter.
* Model selection and per-request model overrides without coupling the agent to one model.

Most tools are declared through configuration, reducing the amount of glue code a development team must maintain.

---

## 3. Example: AWS Support Agent

An AWS Support Agent could be configured to:

* Read logs from Amazon CloudWatch.
* Search AWS documentation.
* Analyze incidents and recommend remediation steps.
* Create a support case when required.

Instead of implementing the agent loop, tool calling, container, and runtime deployment manually, developers primarily define the model, instructions, and permitted tools.

---

## 4. Harness or Runtime?

**AgentCore Harness** is suitable for the common agent pattern: receive a request, reason, call tools, and return a result. It prioritizes development speed and simplicity.

**AgentCore Runtime** is more appropriate when teams need their own framework, custom graphs or workflows, deeper orchestration control, or specialized hooks and logic.

In short: **Harness prioritizes speed**, while **Runtime prioritizes customization**.

---

## 5. Conclusion

AgentCore Harness does not make agent development completely code-free. Developers still need to design prompts, tools, data access, IAM roles, and action controls. However, with orchestration, memory, identity, execution environments, and observability provided as managed capabilities, teams can spend more time solving the actual business problem.

Instead of building the agent’s entire foundation, teams can begin with **CreateHarness** to define it and **InvokeHarness** to put it to work.

---

## Further Reading

Read the official AWS article:
[Amazon Bedrock AgentCore harness is now generally available: Go from idea to production-grade agent in minutes](https://aws.amazon.com/blogs/machine-learning/amazon-bedrock-agentcore-harness-is-now-generally-available-go-from-idea-to-production-grade-agent-in-minutes/)

**#AWS #AmazonBedrock #AgentCore #AgenticAI #GenerativeAI**