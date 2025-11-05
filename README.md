# Building E2E Google ADK Agent Applications - Using Codelabs

This repository contains multiple Google ADK (Agent Development Kit) sample applications demonstrating end-to-end agent development workflows.

## 📁 Projects Overview

### 1. Software Bug Assistant (`/software_bug_assistant/`)
A comprehensive IT support agent that helps triage, manage, and resolve software issues using:
- **PostgreSQL database** for internal ticket management
- **GitHub MCP server** for external issue tracking
- **RAG (Retrieval-Augmented Generation)** for intelligent bug matching
- **Google Search** for external knowledge
- **StackOverflow integration** for community solutions

### 2. Gemini CLI on ADK (`/gemini-cli-on-adk/`)
An advanced development workflow agent that integrates Gemini CLI's non-interactive mode with ADK for:
- **Automated code analysis** without manual file selection
- **Intelligent development task execution**
- **Streamlined codebase insights**
- **Command automation** based on analysis results

## 🚀 Quick Start

### Prerequisites
- Python 3.9+ (3.10+ for Gemini CLI)
- [uv](https://docs.astral.sh/uv/getting-started/installation) package manager
- Git
- Google Cloud CLI (for cloud deployment)

### Choose Your Project

#### Software Bug Assistant
```bash
cd software_bug_assistant
# Follow the detailed setup instructions in the project README
```

#### Gemini CLI on ADK
```bash
cd gemini-cli-on-adk
make install
make playground
```

## 📖 Documentation

Each project contains comprehensive documentation:

- **Software Bug Assistant**: Full setup guide for local and cloud deployment with PostgreSQL, MCP Toolbox, and RAG capabilities
- **Gemini CLI on ADK**: Development workflow automation with Makefile commands and deployment scripts

## 🏗️ Architecture

Both projects demonstrate different aspects of ADK development:

| Feature | Software Bug Assistant | Gemini CLI on ADK |
|---------|----------------------|-------------------|
| **Use Case** | IT Support & Bug Management | Development Workflow Automation |
| **Complexity** | Intermediate | Advanced |
| **Database** | PostgreSQL with RAG | N/A |
| **External APIs** | GitHub, Google Search, StackOverflow | Gemini CLI Integration |
| **Deployment** | Cloud Run + Cloud SQL | Cloud Run |

## 🔧 Development

### Software Bug Assistant Features
- Conversational bug triage and management
- Vector search for duplicate bug detection
- Multi-source information gathering
- Automated ticket creation and updates

### Gemini CLI Integration Benefits
- Intelligent file discovery and analysis
- Automated code generation and testing
- Command execution without manual intervention
- Contextual codebase insights

## 🌟 Getting Started

1. **Clone this repository**
   ```bash
   git clone https://github.com/chandini2595/Building-e2e-google-adk-agent-applications---using-codelabs.git
   cd Building-e2e-google-adk-agent-applications---using-codelabs
   ```

2. **Choose your project and follow the specific README**
   - For bug management: `cd software_bug_assistant && cat README.md`
   - For development automation: `cd gemini-cli-on-adk && cat README.md`

3. **Set up your environment variables**
   - Get Google API key from [AI Studio](https://aistudio.google.com/apikey)
   - Configure project-specific `.env` files

## 📚 Learning Path

1. **Start with Software Bug Assistant** - Learn ADK basics, database integration, and MCP
2. **Progress to Gemini CLI** - Explore advanced workflows and development automation
3. **Deploy to Cloud** - Scale your agents with Google Cloud Run

## 🤝 Contributing

Feel free to contribute improvements, bug fixes, or additional agent examples!

## 📄 License

This project follows the original ADK samples licensing from Google.

---

> **Note**: These are educational samples demonstrating Google ADK capabilities. Adapt the code and configurations for your production use cases.