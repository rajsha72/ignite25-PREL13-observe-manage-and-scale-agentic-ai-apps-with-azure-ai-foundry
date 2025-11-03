# Lab 5: Tracing & Telemetry

Implement observability for your agentic AI application using tracing, telemetry, and Application Insights.

## Description

Learn to instrument your agents with tracing to understand execution flow, collect telemetry for performance monitoring, and analyze agent behavior using span snapshots.

## Learning Objectives

By the end of this lab, you will be able to:

- ✅ Enable tracing for Azure AI agents
- ✅ Collect and analyze span snapshots
- ✅ Understand agent execution flow through traces
- ✅ Monitor performance with Application Insights
- ✅ Debug agent issues using telemetry data

## Prerequisites

- ✅ Completed [Lab 4: Evaluation Metrics](../4-evaluation/)
- ✅ Agents deployed and running
- ✅ Application Insights resource configured

## Key Concepts

### Tracing
Capture detailed execution flow of agent operations:
- **Spans:** Individual operations or steps
- **Traces:** Complete request-response cycles
- **Attributes:** Metadata about operations

### Telemetry
Monitor performance metrics:
- **Latency:** Response times
- **Token Usage:** Cost tracking
- **Error Rates:** Reliability metrics

### Observability
Understand system behavior:
- Debug complex multi-agent interactions
- Identify performance bottlenecks
- Track costs and resource usage

## Copilot Prompts

```
Show me how to enable tracing for Azure AI agents
```

```
Help me analyze span snapshots to understand agent execution flow
```

```
Explain how to integrate Application Insights with Azure AI Foundry
```

```
Show me how to track token usage and costs across agent sessions
```

## Related Resources

- 📘 [Tracing in Azure AI Foundry](https://learn.microsoft.com/azure/ai-foundry/how-to/develop/trace-agents-sdk)
- 📘 [Application Insights Integration](https://learn.microsoft.com/azure/ai-foundry/how-to/application-insights)
- 📘 [OpenTelemetry for AI](https://learn.microsoft.com/azure/ai-foundry/concepts/trace)

## Next Steps

After completing this lab:

**[Lab 6: Deployment & Insights →](../6-deployment/)**

---

[← Previous Lab](../4-evaluation/){ .md-button }
[Next Lab →](../6-deployment/){ .md-button .md-button--primary }
