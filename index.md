---
title: Introduction
layout: home
nav_order: 1
---

# Microsoft AI Agentic Workshop

This workshop teaches you how to design, build, govern, and operate AI applications and agents using Microsoft Foundry, Microsoft Agent Framework, Microsoft 365 Copilot, Copilot Studio, MCP, and A2A. You will learn how to create AI-powered applications that can use models, tools, memory, enterprise data, and multi-agent orchestration while applying observability, evaluation, security, and governance practices.

## Exercises

The hands-on guide uses the **Zava retail assistant** scenario. Each exercise is listed in the left navigation:

| Exercise | What you'll build |
|:--|:--|
| **Exercise 01 - Deploy and configure resources** | Provision Microsoft Foundry, Cosmos DB, Azure AI Search, Application Insights, and Container Apps using Bicep + `azd` |
| **Exercise 02 - Implement a multimodal AI shopping assistant** | Build a single-agent then multi-agent flow with models, tools, and a chat UI |
| **Exercise 03 - Extend the shopping assistant with A2A** | Expose an agent card, run an A2A server, connect specialized agents |
| **Exercise 04 - Observe model utilization in Microsoft Foundry** | Connect Application Insights, inspect traces, token usage, dashboards, evaluations |
| **Exercise 05 - AI-enhanced red teaming** | Run automated red-team scans, analyze failures, apply safety + guardrail improvements |
| **Exercise 06 - Resource cleanup** | Remove workshop resources |

## What we cover

The workshop pairs concept sessions with the exercises above. Use the references in each topic to extend or replace a section for a given audience.

### 1. Standard protocols, prompt & context engineering
MCP, A2A, Azure MCP Server, and security boundaries. MCP exposes tools and enterprise systems through a standard tool interface. A2A handles agent discovery and agent-to-agent communication via agent cards, messages, tasks, and streaming updates.
- [Build and register an MCP server](https://learn.microsoft.com/azure/foundry/mcp/build-your-own-mcp-server)
- [Foundry MCP Server security best practices](https://learn.microsoft.com/azure/foundry/mcp/security-best-practices)
- [A2A protocol specification](https://a2a-protocol.org/latest/)
- [A2A integration in Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/integrations/a2a?pivots=programming-language-python)

### 2. Low-code agents (M365 Copilot + Copilot Studio)
Compare pro-code Foundry agents with low-code Copilot Studio agents. Skippable when attendees don't have a Microsoft 365 tenant.
- [Microsoft Copilot Studio documentation](https://learn.microsoft.com/microsoft-copilot-studio/)
- [Publish agents to Microsoft 365 Copilot](https://learn.microsoft.com/azure/foundry/agents/how-to/publish-copilot)

### 3. Pro-code: Microsoft Foundry platform overview
Foundry projects (Hub vs next-gen Standalone), Agent Service, SDKs & APIs, the 1K+ model catalog, and Model Router. Three agent types: **Prompt**, **Workflow**, **Hosted**. Maps to **Exercise 01**.
- [Microsoft Foundry Agent Service](https://learn.microsoft.com/azure/foundry/agents/overview)
- [Agent development lifecycle](https://learn.microsoft.com/azure/foundry/agents/concepts/development-lifecycle)
- [Deploy your first Hosted agent](https://learn.microsoft.com/azure/foundry/agents/quickstarts/quickstart-hosted-agent)

### 4. Building agents - deep dive
Agent setup (standard + isolated network), the 3 agent types, model selection, Knowledge (Agentic RAG, Foundry IQ), and Tools (MCP, A2A, Responses API, Logic Apps). Maps to **Exercise 02**.
- [Foundry Agent Service tool catalog](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-catalog)
- [Tool best practices](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-best-practice)
- [Connect to MCP servers from Foundry](https://learn.microsoft.com/azure/foundry/agents/how-to/tools/model-context-protocol)
- [Python Agent Framework demos (samples)](https://github.com/Azure-Samples/python-agentframework-demos/tree/main/examples)

### 5. Orchestration, memory & skills
Multi-step reasoning, session vs persistent memory, Agent Skills, and workflow orchestration. For memory, use **Foundry long-term memory** for persistent user/agent facts and **Azure Cosmos DB** as the chat history store.
- [Foundry Agent Service - long-term memory](https://learn.microsoft.com/azure/foundry/agents/concepts/memory)
- [Agent sessions (Microsoft Agent Framework)](https://learn.microsoft.com/agent-framework/agents/conversations/session)
- [Build a chat history store with Azure Cosmos DB](https://learn.microsoft.com/azure/cosmos-db/nosql/ai-chat-history)
- [Microsoft Agent Framework workflows](https://learn.microsoft.com/agent-framework/workflows/)

### 6. Microsoft Agent Framework (MAF)
Patterns, workflow-driven design, tracing/logging/Dev UI, Foundry IQ integration, hosted agents, and LangGraph interop.
- [Microsoft Agent Framework overview](https://learn.microsoft.com/agent-framework/overview/agent-framework-overview)
- [Microsoft Agent Framework GitHub repo](https://github.com/microsoft/agent-framework)
- [Python workflow samples](https://github.com/microsoft/agent-framework/tree/main/python/samples/03-workflows)
- [Foundry hosted agent samples](https://github.com/microsoft/agent-framework/tree/main/python/samples/04-hosting/foundry-hosted-agents)

### 7. Security, guardrails, observability, tracing & evaluations
Content safety, custom guardrails, Entra Agent ID, Agent 365, red teaming, tracing, and evaluations. Maps to **Exercise 04** (observability) and **Exercise 05** (red teaming).
- [Agent tracing overview](https://learn.microsoft.com/azure/foundry/observability/concepts/trace-agent-concept)
- [Monitor AI agents with the Agent Monitoring Dashboard](https://learn.microsoft.com/azure/foundry/observability/how-to/how-to-monitor-agents-dashboard)
- [AI Red Teaming Agent](https://learn.microsoft.com/azure/foundry/concepts/ai-red-teaming-agent)
- [Entra Agent ID](https://learn.microsoft.com/entra/identity/agent-id/overview)

### 8. MCP + agent governance (APIM AI Gateway)
APIM AI Gateway in front of Foundry agents and models: MCP tool registry, Model gateway, MCP gateway, A2A gateway, and BYO APIM.
- [GenAI gateway capabilities in API Management](https://learn.microsoft.com/azure/api-management/genai-gateway-capabilities)
- [Token limit policy](https://learn.microsoft.com/azure/api-management/azure-openai-token-limit-policy)
- [Semantic caching policy](https://learn.microsoft.com/azure/api-management/azure-openai-semantic-cache-store-policy)
- [Expose APIs as MCP servers in API Management](https://learn.microsoft.com/azure/api-management/export-rest-mcp-server)

### 9. Azure AI Services for enterprise
AI Search, Document Intelligence, Language, Vision, Speech, Content Understanding, and Content Safety - pre-built and custom.
- [Azure AI Search](https://learn.microsoft.com/azure/search/)
- [Azure AI Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/)
- [Azure AI Content Understanding](https://learn.microsoft.com/azure/ai-services/content-understanding/)
- [Azure AI Content Safety](https://learn.microsoft.com/azure/ai-services/content-safety/)

### 10. Interoperability + Hosted agents (A2A / MCP)
Orchestrate across MAF, LangGraph, CrewAI, Foundry, and Copilot - no lock-in. Host an external agent inside Foundry and expose it via A2A. Maps to **Exercise 03**.

Use **`az acr build`** (ACR Tasks) to build and push the hosted-agent container image to Azure Container Registry, then point the Foundry hosted agent at the ACR image:

```bash
az acr build \
  --registry <your-acr-name> \
  --image hosted-agents/my-agent:latest \
  --file Dockerfile .
```

Grant the Foundry project's managed identity the **AcrPull** role on the registry.

- [Hosted agents concept](https://learn.microsoft.com/azure/foundry/agents/concepts/hosted-agents)
- [Deploy your first Hosted agent](https://learn.microsoft.com/azure/foundry/agents/quickstarts/quickstart-hosted-agent)
- [Quickstart: Build and push an image with ACR Tasks (`az acr build`)](https://learn.microsoft.com/azure/container-registry/container-registry-quickstart-task-cli)
- [Multi-agent travel planner with A2A interop (sample)](https://github.com/zhuohanl/multi-agent-travel-planner-a2a-interop)

## Microsoft Documentation References

The workshop content is aligned with the latest Microsoft documentation for:

* [Microsoft Foundry Agent Service](https://learn.microsoft.com/azure/foundry/agents/overview)
* [Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/overview/agent-framework-overview)
* [Agent development lifecycle](https://learn.microsoft.com/azure/foundry/agents/concepts/development-lifecycle)
* [Foundry Agent Service tools](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-catalog)
* [Deploy your first Hosted agent](https://learn.microsoft.com/azure/foundry/agents/quickstarts/quickstart-hosted-agent)
* [Foundry observability for agents](https://learn.microsoft.com/azure/foundry/observability/concepts/trace-agent-concept)
* [A2A integration in Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/integrations/a2a?pivots=programming-language-python)

The lab is available as GitHub pages [here](https://microsoft.github.io/TechWorkshop-L300-AI-Apps-and-agents/).

## Prerequisites

For running this lab you will need:

* An Azure subscription with access to Microsoft Foundry, including permissions to create or use an AI Foundry resource, a Foundry project, model deployments, Azure AI Search, Cosmos DB, Application Insights, Container Apps, Container Registry, Storage, and role assignments. External MCAPS subscriptions are preferred for this workshop. Microsoft EMU accounts and Visual Studio subscriptions may not have sufficient privileges for all Foundry and model deployment steps.
* Model quota in a supported region for `gpt-5-mini` or the currently selected chat model, `text-embedding-3-large`, and `Phi-4` if you complete the optional model deployment steps. Recommended regions for the workshop remain **East US 2**, **Sweden Central**, and **France Central** because they are commonly used by the deployment and red-teaming flows.
* Permissions to grant Azure RBAC roles such as **Azure AI User**, **Storage Blob Data Contributor**, and Cosmos DB data-plane roles to users, managed identities, and Foundry project identities used by the labs.
* A desktop, laptop, virtual machine, or GitHub Codespace with permission to install software and run containers.
* Local tooling: Azure CLI, Azure Developer CLI (`azd`), Git, GitHub CLI, Visual Studio Code, the Bicep extension, Docker Desktop or compatible container tooling, Python 3.10 through 3.13, and `uv`.
* A GitHub account that can fork the repository and configure GitHub Actions repository secrets if you run the deployment workflow sections.
* Optional for expanded agenda sections: access to Microsoft 365 Copilot/Copilot Studio, Azure API Management, Logic Apps connectors for MCP tools, and a non-production environment for red teaming and guardrail testing.
