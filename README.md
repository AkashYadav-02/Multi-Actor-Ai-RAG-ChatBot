# 🤖 Chatbots with LangGraph

This project demonstrates how to build a state-of-the-art, stateful chatbot using **LangGraph**, leveraging the **LangChain** ecosystem and the **Groq API** for high-speed Large Language Model (LLM) inference.

---

## 📝 Overview
Traditional chatbots often struggle with complex state management. This project implements a **StateGraph** architecture to create a more robust and predictable conversational agent.

### 🔑 Key Features
* **State Management:** Uses `TypedDict` and `Annotated` for precise message history management.
* **High-Speed Inference:** Powered by the **Gemma2-9b-It** model via Groq for near-instant responses.
* **Orchestration:** Implements a `StateGraph` moving beyond simple linear chains to cyclic agent behaviors.
* **Observability:** Integrated with **LangSmith** for real-time tracing and debugging.

---

## 🛠️ Technical Architecture
The chatbot follows a graph-based logic:
1. **State Definition:** A schema to hold the list of messages.
2. **Nodes:** A `chatbot` function that calls the LLM.
3. **Edges:** Simple routing from the entry point to the chatbot node.

---

## 🚀 Getting Started

### Prerequisites
To run this notebook/script, you will need:
* A **Groq API Key**
* A **LangSmith API Key** (Optional, for tracing)
* Python 3.10+

### Environment Setup
Install the necessary libraries:
```bash
pip install langgraph langsmith langchain langchain_groq langchain_community
