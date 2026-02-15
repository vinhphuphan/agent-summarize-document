# agent-summarize-document

Production-style AI agent that summarizes PDF and text documents using a local LLM (Ollama), built with clean architecture and tool-based design.

This project is part of my journey to becoming an AI Engineer, focusing on practical, production-oriented patterns rather than toy examples.

---

# Features

* Summarize PDF files
* Summarize text (.txt) files
* Runs fully local using Ollama (no external API required)
* Clean, modular architecture
* Tool-based agent design
* Simple and extensible

---

# Architecture

```
agent-summarize-document/

main.py

agent/
    summarize_agent.py

tools/
    file_loader.py
```

Components:

**tools/file_loader.py**

* Loads PDF
* Loads text files

**agent/summarize_agent.py**

* Handles LLM interaction
* Contains summarization logic

**main.py**

* Entry point
* Orchestrates tool + agent

---

# Requirements

* Python 3.11+
* uv
* Ollama

---

# Setup

## 1. Clone repo

```bash
git clone https://github.com/yourusername/agent-summarize-document.git

cd agent-summarize-document
```

---

## 2. Create virtual environment

```bash
uv venv

source .venv/bin/activate
```

Windows:

```bash
.venv\Scripts\activate
```

---

## 3. Install dependencies

```bash
uv add openai pypdf python-dotenv
```

---

## 4. Install and run Ollama

Install:

https://ollama.com

Pull model:

```bash
ollama pull llama3.2
```

Run:

```bash
ollama run llama3.2
```

---

# Usage

Run agent:

```bash
python main.py
```

Enter file path:

```
Enter file path: example.pdf
```

Output:

```
Summary:
...
```

---

# Example Use Cases

* Summarize research papers
* Summarize financial reports
* Summarize books
* Summarize personal notes

---

# Tech Stack

* Python
* Ollama
* Local LLM
* uv
* PyPDF

---

# Roadmap

Planned improvements:

* [ ] Chunking for large documents
* [ ] Streaming output
* [ ] Chat with document
* [ ] Vector database integration
* [ ] Full RAG pipeline
* [ ] Tool-calling agent

---

# Learning Goals

This project focuses on learning:

* AI agent architecture
* Tool abstraction
* LLM integration
* Production design patterns

---

# Author

Phu

AI Engineer Journey – 2026

---

# License

MIT
