# Lab 4: Evaluation Metrics

Implement comprehensive evaluation for quality, safety, and agent performance using Azure AI evaluation tools.

## Description

Learn to systematically evaluate your agentic AI application using Azure AI's evaluation SDK. Measure quality metrics, safety guardrails, and agent-specific performance indicators.

## Learning Objectives

By the end of this lab, you will be able to:

- ✅ Run evaluations using Azure AI evaluation SDK
- ✅ Measure quality metrics (groundedness, relevance, coherence)
- ✅ Evaluate safety (hate, violence, sexual content, self-harm)
- ✅ Assess agent-specific performance indicators
- ✅ Interpret evaluation results and identify improvements

## Lab Structure

| Notebook | Title | Focus Area |
|----------|-------|------------|
| [41](41-first-evaluation.md) | **First Evaluation** | Introduction to evaluations |
| [42](42-evaluate-quality.md) | **Evaluate Quality** | Groundedness, relevance, coherence |
| [43](43-evaluate-safety.md) | **Evaluate Safety** | Content safety filters |
| [44](44-evaluate-agents.md) | **Evaluate Agents** | Agent-specific metrics |

## Prerequisites

- ✅ Completed [Lab 3: Model Customization](../3-customization/)
- ✅ Evaluation dataset prepared
- ✅ Models deployed and accessible

## Key Concepts

### Quality Metrics
- **Groundedness:** Responses based on source data
- **Relevance:** Answers match user questions
- **Coherence:** Logical flow and readability
- **Fluency:** Natural language quality

### Safety Metrics
- **Hate & Fairness:** No discriminatory content
- **Violence:** No violent or harmful content
- **Sexual:** No inappropriate sexual content
- **Self-Harm:** No self-harm promotion

### Agent Metrics
- **Tool Usage:** Correct tool selection
- **Multi-turn Consistency:** Context maintenance
- **Task Completion:** Goal achievement rate

## Copilot Prompts

```
Show me how to run an evaluation using Azure AI evaluation SDK
```

```
Explain the difference between groundedness and relevance metrics
```

```
Help me interpret evaluation results and identify areas for improvement
```

```
Show me how to evaluate agent performance for multi-turn conversations
```

## Related Resources

- 📘 [Evaluation in Azure AI Foundry](https://learn.microsoft.com/azure/ai-studio/how-to/evaluate-generative-ai-app)
- 📘 [Evaluation Metrics Reference](https://learn.microsoft.com/azure/ai-studio/concepts/evaluation-metrics-built-in)
- 📘 [Azure AI Evaluation SDK](https://learn.microsoft.com/python/api/overview/azure/ai-evaluation-readme)

## Next Steps

After completing this lab:

**[Lab 5: Tracing & Telemetry →](../5-tracing/)**

---

[← Previous Lab](../3-customization/){ .md-button }
[Next Lab →](../5-tracing/){ .md-button .md-button--primary }
