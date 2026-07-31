# Agentic AI with Microsoft Foundry Workshop

## 🎯 Workshop Overview

In this hands-on workshop you'll build an agentic AI assistant using Microsoft Foundry. The agent can search a knowledge base, fill in Word documents, and send emails — all orchestrated through a single Foundry Agent.

### What You'll Build

By the end of this workshop you will have:
- A knowledge base powered by Foundry IQ and Azure AI Search
- A custom tool that fills in Word documents
- A Logic App that sends emails on behalf of the agent
- A fully functional agent that combines all of the above

### Learning Objectives

- Set up Microsoft Foundry and deploy AI models
- Prepare and index documents for RAG (Retrieval-Augmented Generation)
- Use Foundry IQ to create a managed knowledge base
- Build custom agent tools (Word document generation)
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
| [Lab 2: Prepare Your Data Sources](./lab-2-prepare-data-sources.md) | Upload documents to Azure Blob Storage | 10-15 min |
| [Lab 3: Create Knowledge Base with Foundry IQ](./lab-3-create-knowledge-base.md) | Set up AI Search, vector index, and Foundry IQ | 20-30 min |
| [Lab 4: Create a Word Document Tool](./lab-4-word-document-tool.md) | Build a tool that fills in Word templates | 20-30 min |
| [Lab 5: Create an Email Action with Logic Apps](./lab-5-email-logic-app.md) | Create a Logic App that sends emails | 15-20 min |
| [Lab 6: Create and Test the Agent](./lab-6-create-test-agent.md) | Wire everything together and test | 15-20 min |

**Total estimated time**: 95-135 minutes

## Additional Resources

- [Microsoft Foundry Documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/what-is-foundry)
- [Understanding RAG](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview)
- [Azure AI Search](https://learn.microsoft.com/en-us/azure/search/)
- [Azure Logic Apps](https://learn.microsoft.com/en-us/azure/logic-apps/)

## 📄 License

This workshop content is provided for educational purposes.

---

**Ready to begin?** Start with [Lab 1: Set Up Azure Resources](./lab-1-setup-azure-resources.md).
