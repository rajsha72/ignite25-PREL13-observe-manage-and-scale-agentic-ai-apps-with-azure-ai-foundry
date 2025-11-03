# Lab 1: Agent Architecture

Learn to build and orchestrate AI agents using Azure AI Agent Service and Microsoft Agent Framework.

## Description

This lab introduces you to two approaches for building AI agents: using the managed Azure AI Agent Service for production deployments, and the flexible Microsoft Agent Framework for development and custom orchestration scenarios.

## Learning Objectives

By the end of this lab, you will be able to:

- ✅ Create agents using Azure AI Agent Service
- ✅ Understand agent conversation threads and message management
- ✅ Implement multi-agent orchestration with Microsoft Agent Framework
- ✅ Compare and choose between Agent Service and Agent Framework approaches
- ✅ Configure agent instructions, tools, and behaviors

## Lab Structure

| Notebook | Title | Focus Area |
|----------|-------|------------|
| [11](11-agent-service.md) | **Agent Service Creation** | Azure AI Agent Service, managed infrastructure |
| [12](12-agent-framework.md) | **Agent Framework Orchestration** | Microsoft Agent Framework, custom workflows |

## Prerequisites

- ✅ Completed [Lab 0: Setup & Validation](../0-setup/)
- ✅ Understanding of the [Zava Scenario](../0-setup/scenario.md)
- ✅ Azure AI Foundry project with deployed models

## Key Concepts

### Azure AI Agent Service

A **managed platform** for deploying production-ready agents with:
- Persistent conversation threads
- Built-in tool orchestration
- Enterprise security and compliance
- Integrated observability

### Microsoft Agent Framework

An **open-source SDK** providing:
- Maximum flexibility and control
- AI-agnostic architecture
- Custom deployment options
- Lightweight abstractions

## Copilot Prompts

```
Explain the differences between Azure AI Agent Service and Microsoft Agent Framework
```

```
Show me how to create a basic agent with Azure AI Agent Service in Python
```

```
Help me implement multi-agent orchestration using Agent Framework
```

```
What are best practices for managing agent conversation state?
```

## Related Resources

- 📘 [Azure AI Agent Service Overview](https://learn.microsoft.com/azure/ai-foundry/agents/overview)
- 📘 [Microsoft Agent Framework Documentation](https://learn.microsoft.com/microsoft-365/agents-sdk/agents-sdk-overview)
- 📘 [Build Collaborative Multi-Agent Systems](https://learn.microsoft.com/azure/ai-foundry/agents/how-to/connected-agents)
- 📘 [Trace AI Agents in Azure AI Foundry](https://learn.microsoft.com/azure/ai-foundry/how-to/develop/trace-agents-sdk)

## Next Steps

After completing this lab:

**[Lab 2: Model Context →](../2-models/)**

---

[← Previous Lab](../0-setup/){ .md-button }
[Next Lab →](../2-models/){ .md-button .md-button--primary }
