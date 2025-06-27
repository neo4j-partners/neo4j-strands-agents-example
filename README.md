# Strands Agent + Neo4j Integration

This project demonstrates the use of a **Strands Agent** connected to a **Neo4j graph database**, enabling agents to answer questions, extract knowledge, and reason about structured data stored in a graph format.

## Overview

This module showcases how to:

- Load and configure a `strands` conversational agent.
- Extend the agent with tools for Neo4j graph interaction.
- Ingest data from Neo4j and convert it into memory for the agent.
- Enable querying, summarizing, and contextualizing graph-based knowledge using LLMs.

It uses `strands-agents`, `neo4j`, and `strands-agents-tools`, with support from `python-dotenv` for environment variables.

---

## Features

- 🔗 **Graph-Aware Agent**: The agent is augmented with tools to query Neo4j directly.
- 🧠 **Memory Support**: Converts graph entities and relationships into structured memory for natural reasoning.
- 🤖 **Multi-turn Chat**: Use the agent in a conversational loop with persistent memory.
- 📄 **Data Extraction**: Automatically extracts nodes and relationships as memory facts.
- 🔍 **Question Answering**: Supports QA over the graph and memory using LLM-based prompts.

---

## Files

- `strands-agent-neo4j.ipynb` — The main notebook demonstrating the pipeline.
- `requirements.txt` — Dependencies for the project.
- `README.md` — This file.

---

## Setup

1. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

2. **Set environment variables** (via `.env` or system environment):

   ```
   NEO4J_URI=bolt://localhost:7687
   NEO4J_USERNAME=neo4j
   NEO4J_PASSWORD=your_password
   ```

3. **Run the notebook**:

   Launch `strands-agent-neo4j.ipynb` and execute cells sequentially.

---

## Tech Stack

- **Python**
- **Neo4j** (Graph Database)
- **Strands Agents** ([repo](https://github.com/neo4j-partners/strands-neo4j-agent))
- **LangChain-style tool interface**
- **Jupyter Notebook**

---

## Use Cases

- Conversational querying over graph databases.
- Auto-generating summaries or insights from graph data.
- Building intelligent assistants for knowledge graphs.
- Enabling LLMs to reason over structured relational data.

---

## Example Usage

Example prompt to the agent:

```text
"Who are the top 3 most connected nodes in the graph?"
```

The agent will use memory and graph tools to respond intelligently.

---

## Development Notes

- Uses `strands-agents-tools.neo4j` for connecting and querying Neo4j.
- Memory is created using both extracted nodes and relationships.
- Agent chain integrates tools dynamically.

---

## License

Apache License 2.0

---

## Author

Guhan Sivaji  
[Neo4j Enterprise]
