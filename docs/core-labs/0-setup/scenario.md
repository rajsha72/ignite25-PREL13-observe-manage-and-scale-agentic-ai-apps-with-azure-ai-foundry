# Zava Enterprise Retailer: Application Scenario

## Business Context

**Zava** is an enterprise retailer specializing in home-improvement goods for DIY enthusiasts. With both physical stores and online shopping capabilities, Zava serves a diverse customer base ranging from weekend hobbyists to professional contractors.

### The Challenge

As Zava's business grows, their customer service team is overwhelmed with:
- Product inquiries and recommendations
- Technical specifications and alternatives for out-of-stock items
- Loyalty program questions and discount calculations
- Order status and return policy questions

**The Solution:** Build an AI-powered customer service chatbot that can handle these inquiries autonomously, improving customer satisfaction while reducing operational costs.

---

## Business Requirements

The Zava customer service chatbot must:

### 🎯 Core Capabilities

1. **Product Assistance** - Help customers find the right products for their needs
2. **Technical Information** - Provide accurate specs and suggest alternatives for out-of-stock items
3. **Personalized Discounts** - Recommend discounts based on customer history, inventory, and cart

### ✨ Quality Standards

- **Helpful Tone:** Respond in a polite, helpful manner consistent with Zava's brand
- **Factual Information:** Ground all responses in actual product catalog data
- **Cost Effectiveness:** Optimize model costs to match task complexity
- **Complex Reasoning:** Handle multi-step discount calculations accurately
- **Scalability:** Manage varying customer volumes reliably and securely

---

## Business Value

By implementing this agentic AI solution, Zava expects to:

- ✅ **Reduce Response Times** - Immediate answers to common customer questions
- ✅ **Increase Sales** - Better product recommendations and personalized offers
- ✅ **Improve Satisfaction** - Consistent, accurate, 24/7 customer support
- ✅ **Lower Costs** - Reduce operational costs compared to human-only support
- ✅ **Scale Operations** - Handle increased volume without proportional cost increases

---

## Three-Agent Architecture

To meet these requirements, Zava implements a **multi-agent system** with three specialized agents:

### 1. 🤝 Customer QA Agent (Polite & Helpful)

**Purpose:** Handle general customer inquiries with a friendly, professional tone

**Capabilities:**
- Answer questions about products, orders, and policies
- Maintain conversational context across multiple turns
- Escalate to human agents when necessary

**Tone:** Polite, empathetic, and helpful

**Example Interaction:**
> **Customer:** "Do you have winter jackets?"  
> **QA Agent:** "I'd be happy to help you find the perfect winter jacket! We have several options available. May I ask what features are most important to you—warmth, waterproofing, or a specific style?"

---

### 2. 📦 Inventory Agent (Technical Information)

**Purpose:** Provide accurate technical product information and stock availability

**Capabilities:**
- Access real-time inventory database
- Retrieve detailed product specifications
- Suggest alternatives for out-of-stock items
- Search product catalog with semantic understanding

**Tone:** Precise and informative

**Example Interaction:**
> **Customer:** "Do you have the blue winter jacket in large?"  
> **Inventory Agent:** "The Arctic Pro Winter Jacket in Ocean Blue (SKU: WJ-2024-BL-L) is currently out of stock. However, we have the same model in Navy Blue (SKU: WJ-2024-NV-L) available, or the Arctic Pro in Ocean Blue in XL size (SKU: WJ-2024-BL-XL) if you'd like to try a larger fit."

---

### 3. 🎁 Loyalty Agent (Customer Personalization)

**Purpose:** Manage customer accounts and provide personalized offers

**Capabilities:**
- Access customer purchase history and loyalty tier
- Calculate context-aware discounts based on cart and inventory
- Apply complex business rules for promotions
- Track and reward loyalty program participation

**Tone:** Personalized and reward-focused

**Example Interaction:**
> **Customer:** "Can I use my points for this purchase?"  
> **Loyalty Agent:** "Great news! As a Gold member with 2,500 points, you qualify for our Winter Sale discount. I can apply a 15% discount to your Arctic Pro Jacket, bringing the price from $149.99 to $127.49. You'll also earn an additional 128 points on this purchase!"

---

## Agent Orchestration Patterns

The three agents work together using different orchestration patterns:

### Sequential Handoff
One agent delegates to another based on the customer's needs:
```
Customer Query → QA Agent → Inventory Agent → Loyalty Agent → QA Agent (final response)
```

### Parallel Processing
Multiple agents analyze the same request simultaneously:
```
Customer Query → [QA Agent + Inventory Agent + Loyalty Agent] → Synthesized Response
```

### Hierarchical Coordination
A coordinator agent delegates to specialized sub-agents:
```
Coordinator → QA Agent (general questions)
           → Inventory Agent (product info)
           → Loyalty Agent (discounts)
```

---

## Workshop Implementation

In this workshop, you'll implement key components of this system:

| Lab | What You'll Build |
|-----|-------------------|
| **Lab 1** | Create single agents with Azure AI Agent Service |
| **Lab 2** | Generate synthetic datasets for model evaluation |
| **Lab 3** | Fine-tune models for Zava's specific tone and format |
| **Lab 4** | Evaluate agent quality, safety, and performance |
| **Lab 5** | Implement tracing and observability |
| **Lab 6** | Deploy and monitor in production |

Given time constraints, you'll implement a **subset of these features**. However, you'll gain the understanding and tools to explore the complete solution on your own.

---

## Technical Architecture

### Azure Services Used

- **Azure AI Foundry** - Central hub for AI development
- **Azure AI Agent Service** - Managed agent infrastructure
- **Azure OpenAI Service** - GPT-4o and GPT-4o-mini models
- **Azure AI Search** - Product catalog semantic search
- **Application Insights** - Monitoring and telemetry
- **Azure Key Vault** - Secure credential management

### Data Sources

- **Product Catalog** - ~1,000 home improvement products with specs
- **Customer Database** - Purchase history and loyalty tier info
- **Inventory System** - Real-time stock levels
- **Discount Rules** - Complex business logic for promotions

---

## Success Metrics

Zava will measure success using:

- **Response Accuracy** - % of queries answered correctly
- **Customer Satisfaction** - CSAT scores from post-interaction surveys
- **Resolution Rate** - % of queries resolved without human escalation
- **Response Time** - Average time to first response
- **Cost per Interaction** - Model + infrastructure costs
- **Conversion Rate** - % of chatbot interactions leading to purchases

---

## Real-World Considerations

### Governance & Safety

- **Content Filtering** - Block inappropriate or harmful responses
- **Data Privacy** - Protect customer PII and payment information
- **Audit Logging** - Maintain compliance with regulations
- **Human Oversight** - Monitor and review agent decisions

### Continuous Improvement

- **Feedback Loops** - Learn from customer ratings and corrections
- **A/B Testing** - Compare different agent configurations
- **Model Updates** - Regularly fine-tune with new data
- **Performance Monitoring** - Track metrics and optimize costs

---

## Learn More

- 📘 [Build Collaborative Multi-Agent Systems](https://learn.microsoft.com/azure/ai-foundry/agents/how-to/connected-agents)
- 📘 [AI Agent Orchestration Patterns](https://learn.microsoft.com/azure/architecture/ai-ml/guide/ai-agent-design-patterns)
- 📘 [Transparency Note for Azure Agent Service](https://learn.microsoft.com/azure/ai-foundry/responsible-ai/agents/transparency-note)

---

[← Back to Setup](index.md){ .md-button }
[Continue to Workshop Outline →](../outline.md){ .md-button .md-button--primary }
