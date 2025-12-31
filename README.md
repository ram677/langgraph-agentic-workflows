# LangGraph Agentic Workflows

A structured, hands-on repository covering LangGraph fundamentals to advanced agentic AI systems.  
This project demonstrates how to design, orchestrate, debug, and evaluate graph-based AI agents using LangGraph, LangChain, and modern LLM tooling.

---

## Repository Structure

```
langgraph-agentic-workflows/
├── 01_basics/
├── 02_advanced/
├── 03_debugging/
├── 04_workflows/
├── 05_human_in_loop/
├── 06_rag/
├── requirements.txt
├── README.md
└── .env
```

---

## Topics Covered

### 01. LangGraph Basics
- Simple graphs
- Chatbots
- Dataclass and Pydantic state schemas
- Tool-enabled agents
- ReAct agents

### 02. Advanced LangGraph
- Streaming responses

### 03. Debugging
- LangGraph API debugging
- Agent execution tracing
- Groq-based agent experimentation

### 04. Workflow Patterns
- Prompt chaining
- Parallelization
- Routing
- Orchestrator–Worker pattern
- Evaluator–Optimizer loop

### 05. Human-in-the-Loop
- Human approval and intervention workflows

### 06. Retrieval-Augmented Generation (RAG)
- Agentic RAG
- Corrective RAG
- Adaptive RAG

---

## Tech Stack

- Python
- LangGraph
- LangChain
- OpenAI (ChatGPT)
- Groq API
- Jupyter Notebook
- python-dotenv

---

## Environment Setup

### Create Virtual Environment

**Windows**
```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables (.env Setup)

Create a `.env` file in the root directory and add the following:

```env
OPENAI_API_KEY=your_openai_api_key_here
GROQ_API_KEY=your_groq_api_key_here
LANGCHAIN_API_KEY=your_langsmith_api_key_here
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=langgraph-agentic-workflows
```

### Key Details
- OPENAI_API_KEY → ChatGPT models via LangChain
- GROQ_API_KEY → Groq-hosted LLM inference
- LANGCHAIN_API_KEY → Optional (LangSmith tracing)
- LANGCHAIN_TRACING_V2 → Enables observability
- LANGCHAIN_PROJECT → LangSmith project name

---

## Loading Environment Variables in Code

Add this at the top of your Python scripts or notebooks:

```python
from dotenv import load_dotenv
load_dotenv()
```

LangChain and LangGraph will automatically pick up the keys.

---

## Verify Setup (Optional)

```python
import os
print(os.getenv("OPENAI_API_KEY") is not None)
print(os.getenv("GROQ_API_KEY") is not None)
```

Both should return `True`.

---

## Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Or open notebooks directly in VS Code.

---

## Security Best Practices

- Never commit `.env` files
- Ensure `.env` is listed in `.gitignore`
- Rotate keys if exposed

---

## Learning & Career Objective

This repository is designed to build strong foundations in agentic AI systems, graph-based reasoning, and production-grade GenAI workflows, while preparing for GenAI and LLM Engineer roles.

---

## License

This project is intended for educational and learning purposes.
