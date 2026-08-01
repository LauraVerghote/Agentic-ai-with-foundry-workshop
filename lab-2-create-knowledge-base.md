# Lab 2: Create a Knowledge Base

[← Back to Workshop Overview](./README.md) | [← Previous: Lab 1](./lab-1-setup-azure-resources.md) | [Next: Lab 3 →](./lab-3-create-agent.md)

---

**⏱️ Estimated Time**: 15-20 minutes

## Overview

In this lab, you'll create a **knowledge base** using **Foundry IQ**, the managed knowledge layer in Microsoft Foundry. You'll upload documents directly and Foundry IQ will handle storage, indexing, and vectorization automatically.

No separate storage account or AI Search setup needed. Foundry IQ manages everything for you.

---

## 🎓 Key Concepts

### What is Foundry IQ?

Foundry IQ is a managed knowledge layer that connects your enterprise data to AI agents:

- **Direct file upload**: Upload documents without needing a separate storage account
- **Automatic vectorization**: Your documents are automatically chunked, embedded, and indexed
- **Agentic retrieval**: Complex questions are automatically decomposed into subqueries
- **Grounded answers with citations**: Returns extractive data with sources

### How It Works

```mermaid
flowchart LR
    A["Upload Documents"] --> B["Foundry IQ"]
    B --> C["Chunking & Embedding"]
    C --> D["Vector Index (AI Search)"]
    D --> E["Agent queries knowledge"]
```

### Supported File Types

Foundry IQ supports: **PDF, DOCX, MD, TXT, JSON, CSV**, and more (up to 50 MB per file).

---

## Step 1: Navigate to Knowledge (Foundry IQ)

1. In the **Microsoft Foundry** portal, make sure you're in your project (`company-assistant`)
2. In the left navigation under **Build**, click **Knowledge**

You'll see the **Knowledge (Foundry IQ)** page with two tabs: Knowledge bases and Indexes.

---

## Step 2: Connect a Foundry IQ Resource

The first time you use Knowledge, you'll need to connect an AI Search resource:

1. Click **Create new resource**
2. In the dialog that appears:
   - **Resource name**: Leave the auto-generated name (e.g., `company-assistant-srch-xxxxx`)
   - **Subscription**: Select your subscription
   - **Resource group**: `rg-foundry-workshop-[yourname]`
   - **Region**: Choose a region that has capacity (if you see a "region at capacity" warning, try another region like **West US 2** or **North Central US**)
3. Check the **acknowledgment checkbox** about additional costs
4. Click **Create**

A "Setting up secure access" dialog will appear, showing that Foundry is granting the necessary RBAC roles (Search Service Contributor). Wait for it to complete.

> 💡 This creates an Azure AI Search resource and configures the managed identity permissions automatically.

![Knowledge page with Foundry IQ resource connected](./images/knowledge-base-created.png)

---

## Step 3: Create a Knowledge Base

1. Click **Create a knowledge base**
2. Fill in the basic configuration:
   - **Name**: `company-knowledge-base`
   - **Description**: `Company information and policies for the chatbot agent`
   - **Chat completions model**: Select `gpt-5.4-mini` (from your deployments)
   - **Retrieval reasoning effort**: Leave as `Minimal`
   - **Output mode**: Leave as `Extractive data`

---

## Step 4: Add a Knowledge Source and Upload Files

1. In the **Knowledge sources (Foundry IQ)** section, click **Upload files**
2. A "Create a knowledge source" dialog appears:
   - **Source type**: File (Preview), "Upload files directly, no storage account needed"
   - **Name**: `company-docs`
   - **Embedding model**: `text-embedding-3-small` should be auto-selected
3. In the **Drop files here or browse** area, upload both files from the `data/knowledge_base/` folder:
   - `company_info.txt`
   - `policies.txt`
4. Click **Create**

> ⚠️ **If upload fails**: Wait 2-3 minutes for the managed identity permissions to propagate, then click **Retry**. The search service needs time for its "Cognitive Services User" role assignment to take effect.

---

## Step 5: Save the Knowledge Base

1. Once you see **"Uploaded 2 files to company-docs"** in the success notification, verify:
   - The knowledge source shows **"Active"** status
   - File count shows **"2 files"**
2. Click **Save knowledge base** at the top right

You're now on the knowledge base detail page showing your configured `company-knowledge-base`.

---

## ✅ What You Accomplished

In this lab, you:

- ✅ Created a Foundry IQ resource (Azure AI Search) with automated RBAC
- ✅ Created a knowledge base with `gpt-5.4-mini` for reasoning
- ✅ Uploaded documents directly (no storage account needed!)
- ✅ Files are automatically chunked, embedded with `text-embedding-3-small`, and indexed

Your knowledge base is now ready to be connected to an agent in the next lab.

---

## 💡 Tips

- **Adding more documents later**: You can always come back and click "Upload files" to add more documents to the knowledge source.
- **Multiple knowledge sources**: A single knowledge base can have multiple sources (files, SharePoint, web URLs). You can click "Add sources" to connect additional data.
- **Different data sources**: In a real scenario, you might connect SharePoint document libraries or OneLake data instead of uploading files directly.

---

## 🔧 Troubleshooting

### 403 Forbidden when connecting knowledge base to agent

If you get a "403 Forbidden" error in Lab 3 when testing the agent with the knowledge base, the **project's managed identity** needs RBAC roles on the AI Search service:

1. Go to the **Azure Portal** → Your AI Search resource
2. Click **Access control (IAM)** → **Add role assignment**
3. Assign **Search Index Data Reader** to your Foundry project's managed identity
4. Wait 1-2 minutes for propagation, then retry

> 💡 The project identity is different from the Foundry resource identity. You can find it under your project resource in the Azure Portal → Identity.

---

[Next: Lab 3 - Create Your First Agent →](./lab-3-create-agent.md)
