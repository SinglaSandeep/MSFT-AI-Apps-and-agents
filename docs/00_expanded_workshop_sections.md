---
title: 'Day 2 expanded agenda'
layout: default
nav_order: 8
---

# Day 2 expanded agenda
{: .no_toc }

A customer-ready outline of the Day 2 Microsoft AI Agentic Workshop. Each module pairs a short concept session with the corresponding hands-on lab. The Zava labs (Exercises 01-07) remain the primary guided path; the modules and references below let instructors extend any topic for a given audience.

## Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Agenda at a glance

| Module | Concept session | Hands-on lab |
|:--|:--|:--|
| **M1. Protocols, prompt & context engineering** | MCP, A2A, Azure MCP Server, security | LAB - Create an MCP Server |
| **M2. Low-code agents** | M365 Copilot + Copilot Studio | LAB - Build an agent in Copilot Studio *(optional)* |
| **M3. Microsoft Foundry platform** | Foundry projects, Agent Service, SDKs, model catalog, Model Router | LAB - Provision environment + first Foundry agent |
| **M4. Building agents - deep dive** | 3 agent types, knowledge, tools, hosting | LAB - Agentic RAG with Foundry IQ + Data Agent + Tools |
| **M5. Orchestration, memory & skills** | Session vs persistent memory, Agent Skills, workflows | LAB - Short-term + long-term memory |
| **M6. Microsoft Agent Framework (MAF)** | Patterns, workflows, tracing, Dev UI, LangGraph interop | LAB - Multi-agent orchestration with MAF |
| **M7. Security, guardrails & evaluations** | Content safety, Entra Agent ID, Agent 365, red teaming, tracing | LAB - Guardrails, red teaming, observability, tracing, evaluations |
| **M8. MCP + agent governance (AI Gateway)** | APIM AI Gateway, MCP/Model/A2A gateways, BYO APIM | LAB - APIM + AI Gateway |
| **M9. Azure AI Services for enterprise** | AI Search, Document Intelligence, Language, Vision, Speech, Content Safety | *(demo / discussion)* |
| **M10. Interoperability + Hosted agents** | Cross-framework orchestration (MAF, LangGraph, CrewAI, Foundry, Copilot) | LAB - Hosted agents + A2A / MCP interop |

> **Legend:** Concept sessions are short lecture + demo. **LAB** rows are hands-on exercises. Optional labs are flagged.

---

## M1. Standard protocols, prompt & context engineering

**Concept session.** Cover how MCP, A2A, prompt design, context engineering, and security boundaries fit together. MCP is best for exposing tools and enterprise systems through a standard tool interface. A2A is best for agent discovery and agent-to-agent communication through agent cards, messages, tasks, and streaming updates.

**Lab.** *LAB - Create an MCP Server.* Build and register a custom MCP server, then connect it to a Foundry agent.

**References**

- [Build and register an MCP server](https://learn.microsoft.com/azure/foundry/mcp/build-your-own-mcp-server)
- [Foundry MCP Server security best practices](https://learn.microsoft.com/azure/foundry/mcp/security-best-practices)
- [A2A protocol specification](https://a2a-protocol.org/latest/)
- [A2A integration in Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/integrations/a2a?pivots=programming-language-python)

---

## M2. Low-code agents (M365 Copilot + Copilot Studio)

**Concept session.** Compare pro-code agents in Microsoft Foundry with low-code conversational agents in Copilot Studio. Position Copilot Studio for business users, Foundry for engineering teams, and Microsoft 365 Copilot as the user-facing surface.

**Lab (optional).** *LAB - Build an agent in Copilot Studio.* Create a Copilot Studio agent with knowledge + actions and publish to Teams. **Skip if attendees do not have a Microsoft 365 tenant.**

**References**

- [Microsoft Copilot Studio documentation](https://learn.microsoft.com/microsoft-copilot-studio/)
- [Publish agents to Microsoft 365 Copilot](https://learn.microsoft.com/azure/foundry/agents/how-to/publish-copilot)

---

## M3. Pro-code: Microsoft Foundry platform overview

**Concept session.** Walk through Foundry projects (Hub vs next-gen Standalone), Agent Service architecture, SDK & API fundamentals, the 1K+ model catalog, and Model Router. Position the three agent types you will use in later modules: **Prompt**, **Workflow**, **Hosted**.

**Lab.** *LAB - Provision environment + create your first Foundry agent.* Provision a Foundry project via `azd`, then build and test a Prompt agent in the playground.

**References**

- [Microsoft Foundry Agent Service](https://learn.microsoft.com/azure/foundry/agents/overview)
- [Agent development lifecycle](https://learn.microsoft.com/azure/foundry/agents/concepts/development-lifecycle)
- [Deploy your first Hosted agent](https://learn.microsoft.com/azure/foundry/agents/quickstarts/quickstart-hosted-agent)

---

## M4. Building agents - deep dive

**Concept session.** Cover agent setup (standard + isolated network), the 3 agent types (Prompt / Workflow / Hosted), model selection, Knowledge (Agentic RAG, Foundry IQ), and Tools (MCP, A2A, Responses API, Logic Apps).

**Lab.** *LAB - Agentic RAG with Foundry IQ + Data Agent + Tools.* Ground an agent on enterprise data using Foundry IQ and add MCP + AI Search tools.

**References**

- [Foundry Agent Service tool catalog](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-catalog)
- [Tool best practices](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-best-practice)
- [Connect to MCP servers from Foundry](https://learn.microsoft.com/azure/foundry/agents/how-to/tools/model-context-protocol)
- [Python Agent Framework demos (samples)](https://github.com/Azure-Samples/python-agentframework-demos/tree/main/examples)

---

## M5. Agent orchestration, memory & skills

**Concept session.** Compare multi-step reasoning patterns and the memory tiers: session memory, **Foundry long-term memory** (persistent user/agent memory), AI Search-backed retrieval, and explicit workflow state. Introduce Agent Skills + the Microsoft Agent Skills Plugin.

**Lab.** *LAB - Add short-term and long-term memory to an agent.*

- **Short-term / session memory:** Microsoft Agent Framework session.
- **Long-term memory:** **Foundry long-term memory** for persistent user/agent facts.
- **Chat history store:** **Azure Cosmos DB** (multi-region, low-latency, scales with sessions).

**References**

- [Foundry Agent Service - long-term memory](https://learn.microsoft.com/azure/foundry/agents/concepts/memory)
- [Agent sessions (Microsoft Agent Framework)](https://learn.microsoft.com/agent-framework/agents/conversations/session)
- [Build a chat history store with Azure Cosmos DB](https://learn.microsoft.com/azure/cosmos-db/nosql/ai-chat-history)
- [Microsoft Agent Framework workflows](https://learn.microsoft.com/agent-framework/workflows/)

---

## M6. Microsoft Agent Framework (MAF)

**Concept session.** MAF combines agent abstractions, workflow orchestration, session state, middleware, telemetry, and provider flexibility across Python and .NET. Use it for code-first control, multi-agent workflow patterns, and portability across Foundry and other runtimes. Demo the Dev UI for tracing.

**Lab.** *LAB - Multi-agent orchestration with MAF.* Build a multi-agent workflow with shared state and inspect traces in Dev UI.

**References**

- [Microsoft Agent Framework overview](https://learn.microsoft.com/agent-framework/overview/agent-framework-overview)
- [Microsoft Agent Framework GitHub repo](https://github.com/microsoft/agent-framework)
- [Python workflow samples](https://github.com/microsoft/agent-framework/tree/main/python/samples/03-workflows)
- [Foundry hosted agent samples](https://github.com/microsoft/agent-framework/tree/main/python/samples/04-hosting/foundry-hosted-agents)

---

## M7. Security, guardrails, observability, tracing & evaluations

**Concept session.** Cover the production-readiness loop: identity (Entra Agent ID, Agent 365), content safety + custom guardrails, observability, tracing, evaluations, and red teaming. Workshop Exercises 04 and 06 implement this loop on the Zava agent.

**Lab.** *LAB - Guardrails, red teaming, observability, tracing & evaluations in Foundry.* Apply content safety + custom guardrails, run automated red-team scans, enable tracing, run evaluations, and inspect telemetry end-to-end.

**References**

- [Agent tracing overview](https://learn.microsoft.com/azure/foundry/observability/concepts/trace-agent-concept)
- [Monitor AI agents with the Agent Monitoring Dashboard](https://learn.microsoft.com/azure/foundry/observability/how-to/how-to-monitor-agents-dashboard)
- [AI Red Teaming Agent](https://learn.microsoft.com/azure/foundry/concepts/ai-red-teaming-agent)
- [Entra Agent ID](https://learn.microsoft.com/entra/identity/agent-id/overview)

---

## M8. MCP + agent governance (APIM AI Gateway)

**Concept session.** Position APIM as an AI Gateway in front of Foundry agents and models. Cover the gateway patterns: **MCP tool registry**, **Model gateway**, **MCP gateway**, **A2A gateway**, and **BYO APIM** for enterprises with an existing APIM footprint.

**Lab.** *LAB - APIM + AI Gateway.* Front a Foundry agent with APIM AI Gateway and apply rate limit, semantic caching, and token tracking policies.

**References**

- [GenAI gateway capabilities in API Management](https://learn.microsoft.com/azure/api-management/genai-gateway-capabilities)
- [Token limit policy](https://learn.microsoft.com/azure/api-management/azure-openai-token-limit-policy)
- [Semantic caching policy](https://learn.microsoft.com/azure/api-management/azure-openai-semantic-cache-store-policy)
- [Expose APIs as MCP servers in API Management](https://learn.microsoft.com/azure/api-management/export-rest-mcp-server)

---

## M9. Azure AI Services for enterprise

**Concept session.** Survey enterprise-grade Azure AI services that complement Foundry agents: AI Search, Document Intelligence, Language, Vision, Speech, Content Understanding, and Content Safety. Compare pre-built vs custom models.

**References**

- [Azure AI Search](https://learn.microsoft.com/azure/search/)
- [Azure AI Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/)
- [Azure AI Content Understanding](https://learn.microsoft.com/azure/ai-services/content-understanding/)
- [Azure AI Content Safety](https://learn.microsoft.com/azure/ai-services/content-safety/)

---

## M10. Interoperability + Hosted agents (A2A / MCP)

**Concept session.** No lock-in: orchestrate across MAF, LangGraph, CrewAI, Foundry, and Copilot using A2A for agent-to-agent communication and MCP for tool exposure. Host an external (e.g., LangGraph) agent inside Foundry to get managed identity, scaling, and observability.

**Lab.** *LAB - Hosted agents + A2A / MCP interop.* Host an external agent in Foundry, expose it via A2A, and consume tools over MCP.

**Build the hosted-agent container image with `az acr build`**

Use ACR Tasks to build and push the image directly to Azure Container Registry (no local Docker required), then point the Foundry hosted agent at the ACR image.

```bash
# Build and push the hosted-agent container image
az acr build \
  --registry <your-acr-name> \
  --image hosted-agents/my-agent:latest \
  --file Dockerfile .
```

Reference `<your-acr-name>.azurecr.io/hosted-agents/my-agent:latest` in the hosted agent's `agent.yaml` / deployment definition and grant the Foundry project's managed identity the **AcrPull** role on the registry.

**References**

- [Hosted agents concept](https://learn.microsoft.com/azure/foundry/agents/concepts/hosted-agents)
- [Deploy your first Hosted agent](https://learn.microsoft.com/azure/foundry/agents/quickstarts/quickstart-hosted-agent)
- [Quickstart: Build and push an image with ACR Tasks (`az acr build`)](https://learn.microsoft.com/azure/container-registry/container-registry-quickstart-task-cli)
- [Multi-agent travel planner with A2A interop (sample)](https://github.com/zhuohanl/multi-agent-travel-planner-a2a-interop)
- [A2A integration in Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/integrations/a2a?pivots=programming-language-python)

---

## Mapping to the Zava hands-on labs

| Workshop module | Maps to Zava exercise |
|:--|:--|
| M3 Foundry platform | Exercise 01 - Deploy and configure resources |
| M4 Building agents | Exercise 02 - Implement a multimodal AI shopping assistant |
| M10 Interoperability | Exercise 03 - Extend the shopping assistant with A2A |
| M7 Observability + evaluations | Exercise 04 - Observe model utilization in Microsoft Foundry |
| M7 Red teaming | Exercise 06 - Red teaming AI agents |
| All modules | Exercise 07 - Resource cleanup |
