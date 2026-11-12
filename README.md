# 🤖 Supervised Multi-Agent AI Research System

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-orange.svg)](https://python.langchain.com/)
[![Groq API](https://img.shields.io/badge/Groq-Fast_Inference-black.svg)](https://groq.com/)
[![Cohere](https://img.shields.io/badge/Cohere-Reranking-purple.svg)](https://cohere.com/)

An advanced, autonomous AI research system powered by **LangGraph** and **Groq**. This project orchestrates multiple specialized AI agents using a supervisor-based routing architecture to execute complex research tasks. It features a state-of-the-art hybrid RAG (Retrieval-Augmented Generation) pipeline combining dense and sparse retrieval, enhanced by Cohere reranking and an iterative self-correction loop.

## 🚀 Key Features

*   **Supervisor-Based Routing (LangGraph):** A central supervisor agent dynamically evaluates user queries and routes them to specialized worker agents, managing the state and execution flow seamlessly.
*   **Hybrid Retrieval Pipeline:** Combines **FAISS** (dense vector search) and **BM25** (sparse keyword search) to maximize document retrieval accuracy across diverse and complex query types.
*   **Intelligent Reranking:** Integrates **Cohere Rerank** to re-evaluate and order the retrieved context, ensuring the generation model only processes the most highly relevant information.
*   **Iterative Feedback Loop:** Built-in reflection mechanism with a 3-attempt validation loop. The system reviews its own research outputs and recursively refines the answers before final delivery to minimize hallucinations.
*   **High-Speed Inference:** Leverages the **Groq API** to execute complex multi-agent reasoning steps with near-instant latency.

## 🧠 System Architecture

1.  **Query Ingestion:** The user submits a research prompt.
2.  **Supervisor Node:** Analyzes the intent and delegates the task to the appropriate specialized agent.
3.  **Hybrid RAG Execution:**
    *   *FAISS* fetches semantically similar contexts.
    *   *BM25* fetches exact keyword matches.
4.  **Context Reranking:** *Cohere* scores and filters the combined retrieval pool.
5.  **Synthesis & Validation:** The assigned agent generates a response and passes it through a 3-attempt self-correction loop.
6.  **Final Output:** The polished, validated research response is delivered to the user.

## 🛠️ Tech Stack

*   **Core Frameworks:** Python, LangChain, LangGraph
*   **LLM Inference:** Groq
*   **Vector Store & Retrieval:** FAISS, BM25
*   **Reranking Engine:** Cohere
*   **Evaluation:** Agentic Feedback Loops

## ⚙️ Quick Start

### Prerequisites
*   Python 3.10+
*   [Groq API Key](https://console.groq.com/)
*   [Cohere API Key](https://dashboard.cohere.com/)

### Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/awasthypranshu/Supervisor-Based-Multi-AI-System.git](https://github.com/awasthypranshu/Supervisor-Based-Multi-AI-System.git)
   cd Supervisor-Based-Multi-AI-System
