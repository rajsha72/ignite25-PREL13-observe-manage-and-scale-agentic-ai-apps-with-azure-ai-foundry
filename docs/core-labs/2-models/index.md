# Lab 2: Model Context

Learn to select models, generate synthetic datasets, and evaluate model performance for your agentic AI application.

## Description

This lab covers the model selection and evaluation phase of the AI development lifecycle. You'll learn how to generate synthetic datasets for testing and compare different models to find the best fit for your use case.

## Learning Objectives

By the end of this lab, you will be able to:

- ✅ Generate synthetic datasets using AI models
- ✅ Understand model selection criteria (capability, cost, performance)
- ✅ Evaluate multiple models on the same task
- ✅ Compare model outputs and select the optimal model
- ✅ Use Azure AI Foundry's model catalog

## Lab Structure

| Notebook | Title | Focus Area |
|----------|-------|------------|
| [21](21-simulate-dataset.md) | **Simulate Dataset** | Synthetic data generation |
| [22](22-evaluate-models.md) | **Evaluate Models** | Model comparison and selection |

## Prerequisites

- ✅ Completed [Lab 1: Agent Architecture](../1-agents/)
- ✅ Access to Azure AI Foundry model catalog
- ✅ Understanding of prompt engineering basics

## Key Concepts

### Synthetic Data Generation
Create realistic test datasets using AI models to:
- Simulate user queries and edge cases
- Generate evaluation benchmarks
- Test agent behaviors at scale

### Model Selection
Choose the right model based on:
- **Capability:** Task-specific requirements
- **Performance:** Latency and accuracy
- **Cost:** Token pricing and throughput
- **Compliance:** Data residency needs

## Copilot Prompts

```
Show me how to generate synthetic customer service queries using GPT-4o
```

```
Explain how to compare model outputs for the same task in Azure AI Foundry
```

```
Help me evaluate which model is best for my use case based on cost and quality
```

## Related Resources

- 📘 [Azure AI Model Catalog](https://learn.microsoft.com/azure/ai-studio/how-to/model-catalog-overview)
- 📘 [Synthetic Data Generation Best Practices](https://learn.microsoft.com/azure/ai-studio/how-to/data-add)
- 📘 [Model Benchmarks and Evaluation](https://learn.microsoft.com/azure/ai-studio/how-to/evaluate-generative-ai-app)

## Next Steps

After completing this lab:

**[Lab 3: Model Customization →](../3-customization/)**

---

[← Previous Lab](../1-agents/){ .md-button }
[Next Lab →](../3-customization/){ .md-button .md-button--primary }
