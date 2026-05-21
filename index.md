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

The hands-on lab guide currently includes:

* Deploy and configure resources
* Implement a multimodal AI shopping assistant
* Extend the shopping assistant using the A2A Protocol
* Observe model utilization in Microsoft Foundry
* Red teaming AI agents
* Resource cleanup

## Microsoft Documentation References

The workshop content is aligned with the latest Microsoft documentation for:

* [Microsoft Foundry Agent Service](https://learn.microsoft.com/azure/ai-foundry/agents/overview)
* [Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/overview/agent-framework-overview)
* [Agent development lifecycle](https://learn.microsoft.com/azure/ai-foundry/agents/concepts/development-lifecycle)
* [Foundry Agent Service tools](https://learn.microsoft.com/azure/ai-foundry/agents/concepts/tool-catalog)
* [Foundry observability for agents](https://learn.microsoft.com/azure/ai-foundry/observability/concepts/trace-agent-concept)

The lab is available as GitHub pages [here](https://microsoft.github.io/TechWorkshop-L300-AI-Apps-and-agents/).

## Prerequisites

For running this lab you will need:

* An MCAPS subscription with access to Microsoft Foundry. External MCAPS subscriptions are preferred, though internal MCAPS subscriptions should work as well. Microsoft EMU accounts will not have sufficient privileges to perform all of the actions necessary.
* A desktop, laptop, or virtual machine and access to install software on that machine.
