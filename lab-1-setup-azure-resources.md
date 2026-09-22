# Lab 1: Create Your Foundry Project

[← Back to Workshop Overview](./README.md) | [Next: Lab 2 →](./lab-2-create-knowledge-base.md)

---

**⏱️ Estimated Time**: 5-10 minutes

## Overview

The workshop administrator has already provisioned the shared **Microsoft Foundry resource**, the required **model deployments**, and **Azure AI Search**. In this lab, you'll create your own project under that shared Foundry resource.

Your project gives you an isolated workspace for your knowledge connection, knowledge base, agent, tools, and traces while still allowing you to use the resources prepared by the administrator.

---

## 🎓 Key Concepts

### What is Microsoft Foundry?

Microsoft Foundry is a unified AI platform that provides:
- **Project Management**: Organize your AI resources and deployments
- **Model Catalog**: Access to GPT, embedding, and other AI models
- **Development Tools**: Build, test, and deploy AI applications
- **Monitoring**: Track usage, costs, and performance

### Shared Resources and Project Isolation

The administrator has prepared these shared resources:

- A Microsoft Foundry resource
- A chat model deployment, such as `gpt-5.6-sol`
- An embedding model deployment, such as `text-embedding-3-small`
- An Azure AI Search service
- A data source containing the NovaPharma workshop documents

You will create your own **Foundry project** under the shared resource. Project-level configuration is isolated, so the knowledge connection and agent you create will not appear in another participant's project.

---

## What You'll Create

- One Microsoft Foundry project under the administrator-provided Foundry resource

---

## Instructions

> ✏️ **Replace `[yourname]`** with your name or identifier, for example `jsmith`. This keeps your project easy to identify.

### 1. Open the Shared Foundry Resource

1. Go to [Azure Portal](https://portal.azure.com)
2. Search for the Foundry resource name provided by your workshop facilitator
3. Open the resource and confirm that the resource type is **Microsoft Foundry**

### 2. Create Your Project

1. In the Foundry resource menu, under **Resource management**, select **Projects**
2. Click **Create project**
3. Enter a unique project name: `company-assistant-[yourname]`
4. Keep the administrator-provided defaults for the shared Foundry resource and region
5. Click **Create** and wait for the project deployment to finish
6. Open the new project, then click **Go to Foundry portal**
7. Toggle the **New Foundry** experience if prompted

   <img src="images/new-foundry.png" width="800"/>

8. If you are asked to select a project, choose `company-assistant-[yourname]`, then click **Let's go**

### 3. Verify the Shared Model Deployments

1. In the Foundry portal, go to Build on the top right
2. Go to models on the left to see your model deployments
3. Confirm that you can see the administrator-provisioned chat model and embedding model

Do not create or deploy another model. Your project uses the deployments attached to the shared Foundry resource.

### ✅ Checkpoint

You should now have:
- [ ] Access to the administrator-provisioned Foundry resource
- [ ] Your own project: `company-assistant-[yourname]`
- [ ] Access to the administrator-provisioned chat and embedding model deployments


---

[← Back to Workshop Overview](./README.md) | [Next: Lab 2 →](./lab-2-create-knowledge-base.md)
