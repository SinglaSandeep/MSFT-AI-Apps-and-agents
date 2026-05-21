---
title: 'Expanded workshop sections'
layout: default
nav_order: 1.5
---

# Expanded workshop sections

This page maps the broader workshop agenda to the current hands-on labs, current Microsoft documentation, and optional sample repositories. The existing Zava labs remain the primary guided path. The sections below help instructors add discussion, demos, or extensions when the session includes the full agentic AI agenda.

## Standard protocols, prompt engineering, and context engineering

Cover how MCP, A2A, prompt design, context engineering, and security boundaries fit together. MCP is best for exposing tools and enterprise systems through a standard tool interface. A2A is best for agent discovery and agent-to-agent communication through agent cards, messages, tasks, and streaming updates.

Recommended references:

- [Build and register an MCP server](https://learn.microsoft.com/azure/foundry/mcp/build-your-own-mcp-server)
- [Foundry MCP Server security best practices](https://learn.microsoft.com/azure/foundry/mcp/security-best-practices)
- [A2A protocol specification](https://a2a-protocol.org/latest/)
- [A2A integration in Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/integrations/a2a?pivots=programming-language-python)

## Low-code agents with Microsoft 365 Copilot and Copilot Studio

Use this section to compare pro-code agents in Microsoft Foundry with low-code conversational agents in Copilot Studio. Keep the lab optional when attendees do not have the required Microsoft 365 tenant access.

Recommended references:

- [Microsoft Copilot Studio documentation](https://learn.microsoft.com/microsoft-copilot-studio/)
- [Publish agents to Microsoft 365 Copilot](https://learn.microsoft.com/azure/foundry/agents/how-to/publish-copilot)
- [Agent applications in Microsoft Foundry](https://learn.microsoft.com/azure/foundry/agents/how-to/agent-applications)

## Microsoft Foundry platform overview

Use the current Foundry Agent Service model: prompt agents, workflow agents, and hosted agents. A prompt agent is configuration-driven. A workflow agent adds declarative orchestration, branching, and human-in-the-loop steps. A hosted agent is a code-based containerized agent that can use Microsoft Agent Framework, LangGraph, or custom logic while Foundry manages hosting, scaling, identity, and observability.

Recommended references:

- [Microsoft Foundry Agent Service](https://learn.microsoft.com/azure/foundry/agents/overview)
- [Agent development lifecycle](https://learn.microsoft.com/azure/foundry/agents/concepts/development-lifecycle)
- [Foundry Agent Service tools](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-catalog)
- [Deploy your first Hosted agent](https://learn.microsoft.com/azure/foundry/agents/quickstarts/quickstart-hosted-agent)

## Building agents deep dive

Use the Zava labs to show the difference between local application orchestration, Foundry-hosted prompt agents, and code-first agent frameworks. Highlight model selection, tools, knowledge, memory, identity, and monitoring as design choices rather than isolated features.

Recommended references:

- [Microsoft Agent Framework overview](https://learn.microsoft.com/agent-framework/overview/agent-framework-overview)
- [Agent Framework agents overview](https://learn.microsoft.com/agent-framework/agents/)
- [Agent Framework workflows overview](https://learn.microsoft.com/agent-framework/workflows/)
- [Python Agent Framework demos](https://github.com/Azure-Samples/python-agentframework-demos/tree/main/examples)

## Agentic RAG, Foundry IQ, data agents, and tools

Use Exercise 01 and Exercise 02 to connect Cosmos DB, Azure AI Search, embeddings, and tool calls. For optional demos, show how Foundry tools can include Azure AI Search, File Search, function calling, Azure Functions, MCP, OpenAPI tools, and A2A.

Recommended references:

- [Azure AI Search in the Foundry Agent Service tool catalog](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-catalog)
- [Tool catalog](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-catalog)
- [Tool best practices for Foundry Agent Service](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-best-practice)
- [Connect to MCP servers](https://learn.microsoft.com/azure/foundry/agents/how-to/tools/model-context-protocol)

## Agent orchestration, memory, and skills

Use this section to compare session memory, persistent memory, retrieval-backed context, and explicit workflow state. In Microsoft Agent Framework, workflows are the right fit when execution order, branching, checkpointing, or human approval must be controlled explicitly.

Recommended references:

- [Microsoft Agent Framework workflows](https://learn.microsoft.com/agent-framework/workflows/)
- [Agent sessions](https://learn.microsoft.com/agent-framework/agents/conversations/session)
- [Agent tools](https://learn.microsoft.com/agent-framework/agents/tools/)
- [Agent Framework samples and patterns](https://github.com/microsoft/agent-framework/tree/main/python/samples)

## Microsoft Agent Framework

Microsoft Agent Framework is the successor path that combines agent abstractions, workflow orchestration, session-based state, middleware, telemetry, and provider flexibility across Python and .NET. Use it when the application needs code-first control, multi-agent workflow patterns, or portability across Foundry and other agent runtimes.

Recommended references:

- [Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/overview/agent-framework-overview)
- [Microsoft Agent Framework GitHub repository](https://github.com/microsoft/agent-framework)
- [Python workflow samples](https://github.com/microsoft/agent-framework/tree/main/python/samples/03-workflows)
- [Foundry hosted agent samples](https://github.com/microsoft/agent-framework/tree/main/python/samples/04-hosting/foundry-hosted-agents)

## Security, guardrails, observability, tracing, and evaluations

Exercise 04 and Exercise 05 cover the production-readiness loop: observe traces, inspect metrics, evaluate agent quality, red-team safety risks, adjust prompts or guardrails, and repeat. For production discussions, include identity, RBAC, non-production red-team environments, telemetry data handling, and cost controls.

Recommended references:

- [Agent tracing overview](https://learn.microsoft.com/azure/foundry/observability/concepts/trace-agent-concept)
- [Monitor AI agents with the Agent Monitoring Dashboard](https://learn.microsoft.com/azure/foundry/observability/how-to/how-to-monitor-agents-dashboard)
- [AI Red Teaming Agent](https://learn.microsoft.com/azure/foundry/concepts/ai-red-teaming-agent)
- [Foundry guardrails overview](https://learn.microsoft.com/azure/foundry/guardrails/guardrails-overview)

## MCP and agent governance

Use this section to discuss control-plane concerns: tool registry, private tool catalog, agent evaluation, auditability, MCP governance, model gateway patterns, A2A gateway patterns, and AI Gateway in Azure API Management.

Recommended references:

- [Create a private tool catalog](https://learn.microsoft.com/azure/foundry/agents/how-to/private-tool-catalog)
- [Govern MCP tools by using an AI gateway](https://learn.microsoft.com/azure/foundry/agents/how-to/tools/governance)
- [AI Gateway in Azure API Management](https://learn.microsoft.com/azure/api-management/genai-gateway-capabilities)
- [Azure API Management policy reference](https://learn.microsoft.com/azure/api-management/api-management-policies)

## Azure AI services for enterprise

Use this section to position supporting Azure AI services used by agentic applications: Azure AI Search, Document Intelligence, Language, Vision, Speech, Content Understanding, and Content Safety. Tie each service to a tool, grounding, evaluation, moderation, or ingestion role.

Recommended references:

- [Azure AI Search documentation](https://learn.microsoft.com/azure/search/)
- [Azure AI Document Intelligence documentation](https://learn.microsoft.com/azure/ai-services/document-intelligence/)
- [Azure AI Content Understanding documentation](https://learn.microsoft.com/azure/ai-services/content-understanding/)
- [Azure AI Content Safety documentation](https://learn.microsoft.com/azure/ai-services/content-safety/)

## Interoperability and hosted agents

Use the A2A lab as the workshop base and the travel-planner sample as an optional reference for a larger interoperability architecture. The key teaching point is that agent logic can be authored once in a code-first framework, exposed through A2A, connected through MCP or Foundry tools, and hosted in Foundry when operational management is required.

Recommended references:

- [Multi-agent travel planner A2A interoperability sample](https://github.com/zhuohanl/multi-agent-travel-planner-a2a-interop)
- [A2A integration in Microsoft Agent Framework](https://learn.microsoft.com/agent-framework/integrations/a2a?pivots=programming-language-python)
- [Deploy your first Hosted agent](https://learn.microsoft.com/azure/foundry/agents/quickstarts/quickstart-hosted-agent)
- [Hosted agents concept](https://learn.microsoft.com/azure/foundry/agents/concepts/hosted-agents)