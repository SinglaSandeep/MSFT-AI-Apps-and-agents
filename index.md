---
title: Introduction
layout: home
nav_order: 1
---

# Microsoft AI Agentic Workshop

This workshop teaches you how to design, build, govern, and operate AI applications and agents using Microsoft Foundry, Microsoft Agent Framework, Microsoft 365 Copilot, Copilot Studio, MCP, and A2A. You will learn how to create AI-powered applications that can use models, tools, memory, enterprise data, and multi-agent orchestration while applying observability, evaluation, security, and governance practices.

## Agenda

This workshop agenda includes:

* Standard protocols, prompt engineering, and context engineering: MCP, A2A, Azure MCP Server, and security concepts
* Lab: Create an MCP server
* Low-code agent development with Microsoft 365 Copilot and Copilot Studio
* Lab: Build an agent in Copilot Studio (skip this lab if not needed for the session)
* Pro-code Microsoft Foundry platform overview: Foundry projects, Agent Service, Foundry architecture, SDKs, APIs, model catalog, and Model Router
* Lab: Provision the environment and create your first Foundry agent
* Building agents deep dive: prompt agents, workflow agents, hosted agents, model selection, knowledge, tools, MCP, A2A, Responses API, Logic Apps, and hosting patterns
* Lab: Agentic RAG with Foundry IQ, Data Agent, and tools
* Agent orchestration, memory, and skills: session memory, persistent memory, context compression, Agent Skills, and workflow orchestration
* Lab: Add short-term and long-term memory to an agent
* Microsoft Agent Framework: agent patterns, workflow-driven design, tracing, logging, Dev UI, Foundry IQ integration, hosted agents, and LangGraph interoperability
* Lab: Multi-agent orchestration with Microsoft Agent Framework
* Security: guardrails, Entra Agent ID, Agent 365, red teaming, observability, tracing, and evaluations
* Lab: Guardrails, red teaming, observability, tracing, and evaluations in Foundry
* MCP and agent governance: evaluation, control plane, auditability, Agent 365, APIM AI Gateway, MCP tool registry, model gateway, MCP gateway, A2A gateway, and BYO APIM gateway patterns
* Lab: APIM and AI Gateway
* Azure AI Services for enterprise: AI Search, Document Intelligence, Language, Vision, Speech, Content Understanding, custom models, and Content Safety
* Interoperability across Microsoft Agent Framework, LangGraph, CrewAI, Foundry, Copilot, MCP, and A2A
* Lab: Hosted agents with A2A and MCP interoperability

## Exercises

The current hands-on lab guide focuses on the Zava retail assistant scenario and includes:

* Deploy and configure resources
* Implement a multimodal AI shopping assistant
* Extend the shopping assistant using the A2A Protocol
* Observe model utilization in Microsoft Foundry
* Red teaming AI agents
* Resource cleanup

For the broader Day 2 agenda, see [Expanded workshop sections](docs/00_expanded_workshop_sections.md). That page maps the agenda topics to Microsoft documentation, sample repositories, and optional lab extensions for MCP, Copilot Studio, Microsoft Agent Framework, hosted agents, A2A/MCP interoperability, AI Gateway, guardrails, and enterprise Azure AI services.

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
