---
title: 'Exercise 02: Implement a multimodal AI shopping assistant'
layout: default
nav_order: 3
has_children: true
---

# Exercise 02: Implement a multimodal AI shopping assistant

## Scenario

This training will have you implement a customer proof of concept using Microsoft Foundry. The customer in this scenario is Zava, a retail chain that specializes in "do-it-yourself" solutions for home improvement projects. Zava would like to build a shopping assistant that helps customers choose the correct products for their own home improvement projects. Customers will be able to upload images, ask questions regarding the set of products available from Zava, and make purchases, all from a multimodal chat interface.

In this exercise, we will build a series of agents and test them locally before deploying the application code to Azure.

## Objectives

After you complete this exercise, you will be able to:

* Build a chat application that allows customers to research products, add products to a cart, and receive loyalty discounts
* Incorporate multiple AI agents to satisfy specific customer needs
* Deploy applications to Azure from Visual Studio Code

## Duration

* **Estimated Time:** 60 minutes

## Related workshop topics

This exercise maps to the **Building agents** and **Orchestration, memory & skills** modules in the [Introduction](../../index.md). As you go through the tasks, keep these production patterns in mind:

* **Short-term (session) memory** is handled inside the agent runtime (Microsoft Agent Framework session).
* **Long-term memory** for persistent user/agent facts should use **Foundry long-term memory** rather than a custom store.
* **Chat history** for the multimodal UI should be persisted in **Azure Cosmos DB** so sessions survive restarts, scale across regions, and stay low-latency.
* **Tools and knowledge** for the agents are added via the Foundry tool catalog (Azure AI Search, MCP, Logic Apps, OpenAPI, function calling). Reference patterns: [Python Agent Framework demos](https://github.com/Azure-Samples/python-agentframework-demos/tree/main/examples).

References: [Foundry long-term memory](https://learn.microsoft.com/azure/foundry/agents/concepts/memory), [Cosmos DB chat history store](https://learn.microsoft.com/azure/cosmos-db/nosql/ai-chat-history), [Foundry tool catalog](https://learn.microsoft.com/azure/foundry/agents/concepts/tool-catalog).
