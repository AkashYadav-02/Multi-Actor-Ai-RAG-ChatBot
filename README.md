Chatbots with Langgraph
This Google Colab notebook demonstrates how to build a chatbot using Langgraph, leveraging the Langchain ecosystem and the Groq API for the Large Language Model (LLM).

Overview
The notebook covers the following key steps:

Environment Setup: Installation of necessary libraries including langgraph, langsmith, langchain, langchain_groq, and langchain_community.
API Key Configuration: Securely retrieving and setting up API keys for Groq and Langsmith using Colab's user data and environment variables.
LLM Initialization: Instantiating a ChatGroq model, specifically Gemma2-9b-It, to power the chatbot's responses.
Langgraph Setup: Defining the chatbot's state using TypedDict and Annotated for message management.
Graph Construction: Building a simple Langgraph StateGraph with a single chatbot node that uses the initialized LLM to process messages.
Chat Interaction: Implementing a basic interactive loop to send user inputs to the graph and stream the chatbot's responses.
Getting Started
To run this notebook, you will need:

A Groq API Key.
A Langsmith API Key.
Make sure to add these keys to your Colab Secrets (accessible via the '🔑' icon in the left panel) with the names groq_api_key and LANGSMITH_API_KEY respectively.

Usage
Execute the cells sequentially. The final cell will start an interactive chat session in the notebook output where you can converse with the Langgraph-powered chatbot.
