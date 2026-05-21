---
title: 'Exercise 03: Extend the shopping assistant using the A2A Protocol'
layout: default
nav_order: 4
has_children: true
---

# Exercise 03: Extend the shopping assistant using the A2A Protocol

## Scenario

In the previous exercise, you implemented a multimodal AI shopping assistant for Zava using Microsoft Foundry. The assistant allows customers to upload images, ask questions regarding the set of products available from Zava, and make purchases, all from a multimodal chat interface. However, Zava would like to extend the capabilities of the shopping assistant by integrating it with additional AI services and tools. This will allow the assistant to provide more personalized recommendations, improve the accuracy of product searches, and enhance the overall customer experience.

In this exercise, we will use the Agent2Agent (A2A) Protocol to enable communication between multiple AI agents. This will allow us to create a more sophisticated shopping assistant that can leverage the strengths of different AI models and services.

This exercise also acts as the interoperability bridge for the broader workshop agenda. A2A provides agent discovery through agent cards and message-based communication, while MCP provides a standard way to expose tools. Together, they let agent logic built with Microsoft Agent Framework, Foundry, LangGraph, CrewAI, or other runtimes participate in a broader agent ecosystem.

## Objectives

After you complete this exercise, you will be able to:

* Understand the A2A Protocol and its benefits
* Implement A2A communication between multiple AI agents
* Explain how A2A and MCP support cross-framework interoperability and hosted-agent patterns

## Duration

* **Estimated Time:** 40 minutes
