# Agentic AI with Microsoft Foundry Workshop

## 🎯 Workshop Overview

In this hands-on workshop you'll build an agentic AI assistant for a fictional pharmaceutical company (NovaPharma) using Microsoft Foundry. The agent can search a product and regulatory knowledge base, fill in regulatory document templates, and send emails, all orchestrated through a single Foundry Agent.

### What You'll Build

By the end of this workshop you will have:
- A knowledge base with product portfolio and regulatory guidelines, powered by Foundry IQ and Azure AI Search
- A custom tool that fills in product summary report templates
- A Logic App that sends emails on behalf of the agent
- A fully functional regulatory affairs assistant that combines all of the above

### Learning Objectives

- Set up Microsoft Foundry and deploy AI models
- Prepare and index documents for RAG (Retrieval-Augmented Generation)
- Use Foundry IQ to create a managed knowledge base
- Build custom agent tools (regulatory document generation)
- Integrate Logic Apps as agent actions (email)
- Create and test a multi-tool Foundry Agent

## 📋 Prerequisites

- **Azure subscription** with contributor access
- **Microsoft Foundry access**
- A modern web browser

## 🗂️ Workshop Structure

| Lab | Description | Time |
|-----|-------------|------|
| [Lab 1: Set Up Azure Resources](./lab-1-setup-azure-resources.md) | Create Foundry project and deploy models | 15-20 min |
| [Lab 2: Create a Knowledge Base](./lab-2-create-knowledge-base.md) | Upload product and regulatory documents to Foundry IQ | 15-20 min |
| [Lab 3: Create Your First Agent](./lab-3-create-agent.md) | Build a regulatory affairs assistant grounded in your knowledge base | 15-20 min |
| [Lab 4: Create a Word Document Tool](./lab-4-word-document-tool.md) | Enable a tool that fills in product summary templates | 20-30 min |
| [Lab 5: Create an Email Action with Logic Apps](./lab-5-email-logic-app.md) | Create a Logic App that sends emails and attach generated documents | 20-30 min |

**Total estimated time**: 85-120 minutes

## Additional Resources

- [Microsoft Foundry Documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/what-is-foundry)
- [Understanding RAG](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview)
- [Azure AI Search](https://learn.microsoft.com/en-us/azure/search/)
- [Azure Logic Apps](https://learn.microsoft.com/en-us/azure/logic-apps/)

## 📄 License

This workshop content is provided for educational purposes.

---

**Ready to begin?** Start with [Lab 1: Set Up Azure Resources](./lab-1-setup-azure-resources.md).

> **Note**: This workshop uses the **New Foundry** portal experience at [ai.azure.com](https://ai.azure.com). Make sure the "New Foundry" toggle is enabled in the top navigation bar.
