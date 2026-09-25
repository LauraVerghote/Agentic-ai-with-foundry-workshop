# Agentic AI with Microsoft Foundry Workshop

## 🎯 Workshop Overview

In this hands-on workshop you'll build an agentic AI assistant for a fictional pharmaceutical company, NovaPharma, using Microsoft Foundry. The agent searches a product and regulatory knowledge base, then fills a Word document template with grounded information. You'll use tracing and evaluation to inspect and assess the complete workflow.

### What You'll Build

By the end of this workshop you will have:
- Your own project under an administrator-provisioned Foundry resource
- A project-scoped Foundry IQ knowledge base connected to administrator-provisioned Azure AI Search and source documents
- A regulatory affairs agent grounded in product and regulatory content
- A Code Interpreter tool that fills a Product Summary Report Word template
- An end-to-end trace showing knowledge retrieval followed by document generation
- An evaluation of the captured interaction using built-in quality evaluators

### Learning Objectives

- Create a project under a shared Microsoft Foundry resource
- Reuse administrator-provisioned model deployments, Azure AI Search, and source documents
- Connect Foundry IQ and create a project-scoped knowledge base
- Build and test a grounded Foundry Agent
- Use Code Interpreter to generate a Word document from a template
- Inspect traces to verify retrieval and tool execution order
- Evaluate a captured interaction for =relevance, coherence, and fluency

## 📋 Prerequisites

- Access to the Azure subscription and administrator-provisioned Foundry resource used for the workshop
- Permission to create a project under the shared Foundry resource
- Access to the administrator-provisioned model deployments and Azure AI Search service
- A modern web browser

The workshop facilitator provides the names of the shared Foundry resource, Foundry IQ or Azure AI Search resource, and prepared knowledge source or index.

## 🗂️ Workshop Structure

| Lab | Description | Time |
|-----|-------------|------|
| [Lab 1: Create Your Foundry Project](./lab-1-setup-azure-resources.md) | Create a project under the shared Foundry resource and verify model access | 5-10 min |
| [Lab 2: Create a Knowledge Base](./lab-2-create-knowledge-base.md) | Connect Foundry IQ to the prepared Search resource and source data | 10-15 min |
| [Lab 3: Create Your First Agent](./lab-3-create-agent.md) | Build a regulatory affairs assistant grounded in your knowledge base | 15-20 min |
| [Lab 4: Create a Word Document Tool](./lab-4-word-document-tool.md) | Enable Code Interpreter and attach the product summary template | 10-15 min |
| [Lab 5: Trace and Evaluate the Agent Workflow](./lab-5-trace-agent.md) | Verify tool execution order and evaluate the captured interaction | 20-25 min |

**Total estimated time**: 60-85 minutes

## Additional Resources

- [Microsoft Foundry Documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/what-is-foundry)
- [Understanding RAG](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview)
- [Azure AI Search](https://learn.microsoft.com/en-us/azure/search/)
- [Microsoft Foundry Observability](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/observability)

## 📄 License

This workshop content is provided for educational purposes.

---

**Ready to begin?** Start with [Lab 1: Set Up Azure Resources](./lab-1-setup-azure-resources.md).

> **Note**: This workshop uses the **New Foundry** portal experience at [ai.azure.com](https://ai.azure.com). Make sure the "New Foundry" toggle is enabled in the top navigation bar.
