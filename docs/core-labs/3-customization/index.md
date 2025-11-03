# Lab 3: Model Customization

Master fine-tuning, custom evaluation, and model distillation techniques to tailor AI models to your specific requirements.

## Description

Learn how to customize foundation models through fine-tuning to achieve specific behaviors, create custom evaluators for domain-specific quality metrics, and use distillation to optimize model costs.

## Learning Objectives

By the end of this lab, you will be able to:

- ✅ Fine-tune models for specific tones, formats, and behaviors
- ✅ Create custom evaluators for domain-specific metrics
- ✅ Apply distillation to create cost-efficient models
- ✅ Understand when fine-tuning provides value over prompt engineering
- ✅ Evaluate fine-tuned model quality

## Lab Structure

| Notebook | Title | Focus Area |
|----------|-------|------------|
| [31](31-basic-finetuning.md) | **Basic Fine-tuning** | Fine-tune for tone and format |
| [32](32-custom-grader.md) | **Custom Grader** | Domain-specific evaluation |
| [33](33-distill-finetuning.md) | **Distillation Fine-tuning** | Cost optimization through distillation |

## Prerequisites

- ✅ Completed [Lab 2: Model Context](../2-models/)
- ✅ Training dataset prepared
- ✅ Understanding of model evaluation metrics

## Key Concepts

### Fine-Tuning
Train a model on your specific examples to:
- Achieve consistent tone and formatting
- Reduce prompt engineering overhead
- Improve task-specific performance
- Optimize for efficiency

### Custom Evaluators
Create domain-specific quality metrics beyond standard evaluators:
- Business rule compliance
- Brand voice consistency
- Domain-specific accuracy

### Model Distillation
Use a larger model's outputs to train a smaller, more efficient model:
- Lower latency and cost
- Similar task performance
- Efficient use of production data

## Copilot Prompts

```
Explain when I should fine-tune a model vs using prompt engineering
```

```
Show me how to prepare a training dataset for fine-tuning in JSONL format
```

```
Help me create a custom evaluator for measuring politeness in customer service responses
```

```
Explain model distillation and how it can reduce costs
```

## Related Resources

- 📘 [Fine-tune Models in Azure AI Foundry](https://learn.microsoft.com/azure/ai-studio/how-to/fine-tune-model-llama)
- 📘 [Create Custom Evaluators](https://learn.microsoft.com/azure/ai-studio/how-to/develop/evaluate-sdk#custom-evaluators)
- 📘 [Model Distillation Guide](https://learn.microsoft.com/azure/ai-studio/concepts/model-distillation)

## Next Steps

After completing this lab:

**[Lab 4: Evaluation Metrics →](../4-evaluation/)**

---

[← Previous Lab](../2-models/){ .md-button }
[Next Lab →](../4-evaluation/){ .md-button .md-button--primary }
