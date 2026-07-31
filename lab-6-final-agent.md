# Lab 6: Final Agent — Combine All Tools

[← Back to Workshop Overview](./README.md) | [← Previous: Lab 5](./lab-5-email-logic-app.md)

---

**⏱️ Estimated Time**: 15-20 minutes

## Overview

In this final lab, you'll combine everything you've built into a single multi-tool agent that can:
- Answer questions from the knowledge base
- Generate Word documents
- Send emails via Logic Apps

---

## Step 1: Update Agent Instructions

1. Open your `company-chatbot` agent in the **Agents** section
2. Update the instructions to include all capabilities:

```text
You are a helpful company assistant. You have the following capabilities:

1. **Knowledge Base**: Answer questions about company policies, information, and procedures using the connected knowledge base.

2. **Document Generation**: When a user asks you to create or fill in a document, use the Word document tool to generate it.

3. **Email**: When a user asks you to send an email, use the email tool to compose and send it.

Guidelines:
- Always ground factual answers in the knowledge base
- Confirm with the user before sending emails
- Be concise and professional
- If you can't find information in the knowledge base, say so honestly
```

---

## Step 2: Verify All Tools Are Connected

In the agent playground, verify:

- ✅ **Knowledge**: `company-knowledge-base` is connected and Active
- ✅ **Tools**: Word document tool is listed
- ✅ **Tools**: Email (Logic App) tool is listed

---

## Step 3: End-to-End Testing

Test the full agent with these scenarios:

**Scenario 1 — Knowledge retrieval:**
```
What shipping options does the company offer?
```

**Scenario 2 — Document generation:**
```
Create a welcome letter for a new employee named Sarah Johnson who starts on August 15, 2026 in the Engineering department.
```

**Scenario 3 — Multi-step task:**
```
Look up the return policy and then send an email to customer@example.com summarizing it.
```

---

## Step 4: Publish the Agent (Optional)

Once you're satisfied with the agent's behavior:

1. Click the **Publish** button at the top right
2. Choose your publishing target
3. The agent is now available via API for integration into applications

---

## ✅ What You Accomplished

In this workshop, you built a complete agentic AI system:

- ✅ **Lab 1**: Set up Microsoft Foundry with model deployments
- ✅ **Lab 2**: Created a knowledge base with Foundry IQ
- ✅ **Lab 3**: Built your first agent with knowledge grounding
- ✅ **Lab 4**: Added a custom Word document generation tool
- ✅ **Lab 5**: Integrated Logic Apps for email actions
- ✅ **Lab 6**: Combined everything into a multi-tool agent

---

## 🚀 Next Steps

- **Add more data sources**: Connect SharePoint, OneLake, or web URLs to your knowledge base
- **Add guardrails**: Use the Guardrails section to add content safety filters
- **Enable memory**: Turn on the Memory feature for persistent context across sessions
- **Deploy to production**: Use the Publish feature to expose your agent via API
- **Add evaluation**: Set up automated evaluations to measure agent quality

---

## 🧹 Cleanup

If you want to clean up all resources created during this workshop:

1. Go to the **Azure Portal** → **Resource Groups**
2. Find `rg-foundry-workshop-[yourname]`
3. Click **Delete resource group**
4. Type the resource group name to confirm
5. Click **Delete**

This will remove all resources created during the workshop (Foundry resource, AI Search, etc.).

---

**🎉 Congratulations!** You've completed the Agentic AI with Microsoft Foundry workshop!
