# neo4j-strands-agents-example

This project demonstrates how to integrate Neo4j with the AWS Strands Agent framework to explore and analyze a financial crime dataset using multi-agent orchestration.

## Features
- **Agent orchestration** using the Strands Agent SDK
- **Neo4j graph database** for financial crime data
- **AWS Bedrock** for LLM-powered agent reasoning
- **Jupyter notebook** for interactive exploration
- Example notebook for agent queries and orchestration

## Prerequisites
- Python 3.10+
- The notebook uses a publicly hosted [Financial crimes investigation dataset](https://github.com/neo4j-graph-examples/fincen)
- AWS account with Bedrock access
- - [Neo4j Aura](https://neo4j.com/cloud/aura/) or local Neo4j instance if you want to have your own neo4j deployment
- [strands-agents](https://pypi.org/project/strands-agents/) and [strands-agents-tools](https://pypi.org/project/strands-agents-tools/)

## Setup
1. Clone this repository:
   ```sh
   git clone https://github.com/neo4j-partners/strands-neo4j-agent.git
   cd strands-neo4j-demo
   ```
2. Create and activate a Python virtual environment:
   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Copy `.env.example` to `.env` and fill in your AWS and Neo4j credentials.

## Neo4j MCP Server Integration
This project uses the [Neo4j MCP server](https://github.com/neo4j-contrib/mcp-neo4j) to enable secure, programmatic access to your Neo4j database from the Strands Agent framework. The MCP server acts as a bridge between the agent tools and your Neo4j instance.

## Usage
- Open `strands-agent-neo4j.ipynb` in Sagemaker Jupyter Notebook or VS Code for an interactive demo.
- Run the notebook cells to:
  - Connect to Neo4j (via MCP server) and AWS
  - Query the financial crime dataset using LLM agents
  - Explore the results

## Project Structure
- `strands-agent-neo4j.ipynb` — Main notebook demo
- `.env.example` — Example environment variables
- `requirements.txt` — Python dependencies
