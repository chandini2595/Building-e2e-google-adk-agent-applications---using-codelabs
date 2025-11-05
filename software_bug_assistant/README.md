# Software Bug Assistant - ADK Python Sample Agent

[![YouTube](https://img.shields.io/badge/Watch-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://youtu.be/5ZmaWY7UX6k?si=ZbtTScrOls6vp7CH)
[![Google Cloud](https://img.shields.io/badge/Read_Blog-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com/blog/topics/developers-practitioners/tools-make-an-agent-from-zero-to-assistant-with-adk?e=48754805?utm_source%3Dtwitter?utm_source%3Dlinkedin)

## Overview

The Software Bug Assistant is a sample agent designed to help IT Support and Software Developers triage, manage, and resolve software issues. This sample agent uses ADK Python, a PostgreSQL bug ticket database (internal tickets), GitHub MCP server (external tickets), RAG, Google Search, and StackOverflow to assist in debugging. 

![](deployment/images/google-cloud-architecture.png)

This README contains instructions for local and Google Cloud deployment. 

## Agent Details

The key features of the Software Bug Assistant Agent include:

| Feature | Description |
| --- | --- |
| **Interaction Type** | Conversational |
| **Complexity**       | Intermediate |
| **Agent Type**       | Single Agent |
| **Components**       | Tools, Database, RAG, Google Search, GitHub MCP |
| **Vertical**         | Horizontal / IT Support |

## Agent Architecture

<img src="deployment/images/architecture.svg" width="50%" alt="Architecture">

## Key Features

*   **Retrieval-Augmented Generation (RAG):** Leverages Cloud SQL's built-in [Vertex AI ML Integration](https://cloud.google.com/sql/docs/postgres/integrate-cloud-sql-with-vertex-ai) to fetch relevant/duplicate software bugs.
*   **MCP Toolbox for Databases:** [MCP Toolbox for Databases](https://github.com/googleapis/genai-toolbox) to provide database-specific tools to our agent.
*   **GitHub MCP Server:** Connects to [GitHub's remote MCP server](https://github.com/github/github-mcp-server?tab=readme-ov-file#remote-github-mcp-server)
to fetch external software bugs (open issues, pull requests, etc).
*   **Google Search:** Leverages Google Search as a built-in tool to fetch
relevant search results in order to ground the agent's responses with external
up-to-date knowledge.
*   **StackOverflow:** Query [StackOverflow's](https://stackoverflow.com/) powerful Q\&A data, using [LangChain's extensive tools library](https://python.langchain.com/docs/integrations/tools/)— specifically, the [StackExchange API Wrapper tool.](https://python.langchain.com/docs/integrations/tools/stackexchange/). ADK comes with support for [third-party tools like LangChain tools](https://google.github.io/adk-docs/tools/third-party-tools/#1-using-langchain-tools)

## Quick Start

### Prerequisites 
- Python 3.9+
- [uv](https://docs.astral.sh/uv/getting-started/installation) (to manage dependencies)
- PostgreSQL
- Google API key from [AI Studio](https://aistudio.google.com/apikey)
- GitHub Personal Access Token

### Setup
1. **Configure environment variables:**
   ```bash
   echo "GOOGLE_API_KEY=your_api_key_here" >> .env
   echo "GOOGLE_GENAI_USE_VERTEXAI=FALSE" >> .env
   echo "GITHUB_PERSONAL_ACCESS_TOKEN=your_github_token_here" >> .env
   ```

2. **Set up PostgreSQL database:**
   ```bash
   brew services start postgresql
   psql -U postgres
   # Run the SQL commands from the full setup guide below
   ```

3. **Run the agent:**
   ```bash
   uv run adk web
   ```

## Full Setup Guide

For complete setup instructions including:
- Database initialization with sample data
- MCP Toolbox configuration
- Cloud deployment steps
- Troubleshooting guide

Please refer to the comprehensive documentation in the main repository README.

## Example Queries

Try asking the agent:
- "Can you list all open internal ticket issues?"
- "Can you bump the priority of ticket ID 7 to P0?"
- "Are there any discussions on StackOverflow about CVE-2024-3094?"
- "Can you list the latest 5 open issues on the psf/requests GitHub repository?"

## Architecture Diagram

![Software Bug Agent Demo](deployment/images/software-bug-agent.gif)

For detailed deployment instructions, database setup, and cloud configuration, see the main repository documentation.