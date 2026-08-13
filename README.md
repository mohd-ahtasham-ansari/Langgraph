# LangGraph Learning

This repository contains learning materials, experiments, and examples for building stateful, multi-actor applications with LLMs using [LangGraph](https://python.langchain.com/docs/langgraph/). 

## Project Structure

The repository is organized into progressive learning modules via Jupyter Notebooks:

- **`1-Basic_chatbot/`**: Contains `1-Basic_chatbot.ipynb`, which demonstrates how to build a basic chatbot using LangGraph, handling conversation state and simple tool calling.
- **`2-HumanInTheLoop/`**: Contains `2-human_in_the_loop.ipynb`, showing how to implement human-in-the-loop (HITL) workflows. It covers pausing execution with `interrupt`, inspecting the graph state via `MemorySaver`, and allowing a human to approve or modify actions before continuing.

## Setup & Installation

This project supports both standard `pip` and modern package managers like `uv` via the provided configuration files.

1. Clone the repository and navigate to the project root.

2. Create a `.env` file in the root directory and add your API keys (e.g., Tavily, Groq/Mistral, LangChain/LangSmith):
   ```env
   TAVILY_API_KEY=your_tavily_key
   GROQ_API_KEY=your_groq_key
   LANGCHAIN_API_KEY=your_langchain_key
   LANGCHAIN_TRACING_V2=true
   LANGCHAIN_PROJECT=langgraph-learning
   ```

3. Install dependencies:
   
   **Using `uv` (Recommended):**
   ```bash
   uv sync
   ```
   
   **Using `pip`:**
   ```bash
   pip install -r requirements.txt
   ```

## Technologies Used

- **[LangGraph](https://github.com/langchain-ai/langgraph)** for managing cyclic graphs and stateful AI workflows.
- **[LangChain](https://github.com/langchain-ai/langchain)** for core LLM interactions and abstractions.
- **[LangSmith](https://smith.langchain.com/)** for debugging, tracing, and monitoring the agent's behavior.
- **Tavily Search API** for web search tools.

## Getting Started

Open the Jupyter notebooks in the numbered directories to learn the concepts step-by-step. Start with `1-Basic_chatbot` to understand the foundational nodes, edges, and state management in LangGraph before moving on to more advanced human-in-the-loop patterns.
