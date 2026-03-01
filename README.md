# 🤖 Agentic Chatbot Orchestration with LangGraph & Groq

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![LangChain](https://img.shields.io/badge/orchestration-LangChain-green.svg)](https://blog.langchain.dev/)
[![LLM: Gemma2-9b](https://img.shields.io/badge/LLM-Gemma2--9b--It-orange.svg)](https://groq.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Overview
This repository implements a **Stateful AI Agent** using **LangGraph**. Unlike traditional linear LLM chains, this architecture treats conversation as a **Directed Acyclic Graph (DAG)**, allowing for complex state management, cyclic reasoning, and robust error handling.

The system is optimized for low-latency inference using the **Groq LPU™ Inference Engine** and the **Gemma2-9b-It** model.

---

## 🏗️ Architecture & Design Patterns

### 1. Stateful Graph Logic
Instead of passing a simple string back and forth, we manage a `TypedDict` state. This ensures that the message history is immutable and traceable throughout the lifecycle of the request.

### 2. Decision Logic (The "Node" Pattern)
* **Chatbot Node:** Acts as the primary processor, transforming input state into a model response.
* **Message Schema:** Utilizes `Annotated` sequences to ensure that the conversation history persists correctly across loops.

### 3. Observability
Integrated with **LangSmith** for production-grade tracing. This allows us to:
* Monitor token usage and latency.
* Debug "hallucination" points in the graph.
* Visualize the decision-making path of the agent.

---

## 🛠️ Technical Stack
* **Orchestration:** [LangGraph](https://github.com/langchain-ai/langgraph)
* **LLM Provider:** [Groq Cloud](https://console.groq.com/) (Gemma2-9b-It)
* **Tracing/Telemetry:** [LangSmith](https://smith.langchain.com/)
* **Environment:** Python 3.10+, Google Colab / Local VirtualEnv

---

## 🚀 Getting Started

### 1. Installation
```bash
pip install -U langgraph langchain_groq langchain_community langsmith
