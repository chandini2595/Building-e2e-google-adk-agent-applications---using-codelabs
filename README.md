# Building E2E Google ADK Agent Applications - Using Codelabs

This repository contains multiple Google ADK (Agent Development Kit) sample applications demonstrating end-to-end agent development workflows.

## 📁 Projects Overview

### Software Bug Assistant (`/software_bug_assistant/`)
A comprehensive IT support agent that helps triage, manage, and resolve software issues using:
- **PostgreSQL database** for internal ticket management
- **GitHub MCP server** for external issue tracking
- **RAG (Retrieval-Augmented Generation)** for intelligent bug matching
- **Google Search** for external knowledge
- **StackOverflow integration** for community solutions



### Gemini CLI on ADK (`/gemini-cli-on-adk/`)
An advanced development workflow agent that integrates Gemini CLI's non-interactive mode with ADK for:
- **Automated code analysis** without manual file selection
- **Intelligent development task execution**
- **Streamlined codebase insights**
- **Command automation** based on analysis results

### Lead Generation Agent ADK (`/leadGenerationAgentADK/`)
An interactive lead generation system built on an agentic framework that intelligently discovers investment patterns and identifies new leads:
- **Pattern Discovery** - Analyzes successful companies to understand pre-investment signals
- **Lead Generation** - Uses discovered patterns to find high-potential prospects
- **Interactive Workflow** - User-guided decision making at critical points
- **Agentic Architecture** - Hierarchical specialized agents for different tasks
- **Cloud Deployment** - Ready for Google Cloud Agent Engine deployment

### Production Quality Code Review Assistant (`/adk-code-review-assistant/`)
An intelligent, multi-agent code review system powered by Google ADK and Gemini models for comprehensive Python code analysis:
- **Dual-Pipeline Architecture** - Review Pipeline + Fix Pipeline with specialized agents
- **Code Structure Analysis** - AST parsing to identify functions, classes, and structural issues
- **PEP 8 Style Checking** - Automated style validation with weighted scoring
- **Automated Testing** - Generates and executes 15-20 comprehensive test cases
- **Personalized Feedback** - Constructive feedback that adapts based on submission history
- **Automated Code Fixing** - Iterative fix attempts through loop architecture with validation
- **Production Deployment** - Support for Agent Engine, Cloud Run, and GKE deployments

Youtube Links:

https://youtu.be/2GuM02RBbEQ

https://youtu.be/GJIUW8u3AoQ

https://youtu.be/Z7qNeKmhxYA

https://youtu.be/xgp49PzBzcI

https://youtu.be/v0A54Ng5Bg4

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

#### Lead Generation Agent ADK
```bash
cd leadGenerationAgentADK
pip install poetry
poetry install
poetry run adk run LeadGenerationResearch
```

#### Production Quality Code Review Assistant
```bash
cd adk-code-review-assistant
pip install poetry
poetry install
./deploy.sh local  # For local development
# OR
./deploy.sh cloud-run  # For production deployment
```

## 📖 Documentation

Each project contains comprehensive documentation:

- **Software Bug Assistant**: Full setup guide for local and cloud deployment with PostgreSQL, MCP Toolbox, and RAG capabilities
- **Gemini CLI on ADK**: Development workflow automation with Makefile commands and deployment scripts
- **Lead Generation Agent**: Interactive agentic framework for business lead discovery with pattern analysis
- **Code Review Assistant**: Production-quality multi-agent system for comprehensive Python code analysis and automated fixing

## 🏗️ Architecture

All projects demonstrate different aspects of ADK development:

| Feature | Software Bug Assistant | Gemini CLI on ADK | Lead Generation Agent | Code Review Assistant |
|---------|----------------------|-------------------|---------------------|---------------------|
| **Use Case** | IT Support & Bug Management | Development Workflow Automation | Business Lead Discovery | Code Quality & Education |
| **Complexity** | Intermediate | Advanced | Advanced | Production Quality |
| **Database** | PostgreSQL with RAG | N/A | N/A | PostgreSQL/Vertex AI Sessions |
| **External APIs** | GitHub, Google Search, StackOverflow | Gemini CLI Integration | Google Search, Web Research | Built-in Code Execution |
| **Architecture** | Single Agent + MCP | CLI Integration | Multi-Agent Hierarchy | Dual-Pipeline Multi-Agent |
| **Deployment** | Cloud Run + Cloud SQL | Cloud Run | Agent Engine + AgentSpace | Agent Engine + Cloud Run + GKE |

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

### Lead Generation Agent Features
- Interactive pattern discovery from successful companies
- Predictive lead identification using learned patterns
- Multi-phase agentic workflow (learning → prediction)
- User-controlled decision points for quality assurance
- Comprehensive reporting with sources and analysis

### Code Review Assistant Features
- Comprehensive Python code analysis with AST parsing
- PEP 8 style checking with detailed violation reports
- Automated test generation and execution (15-20 tests per submission)
- Personalized feedback with improvement tracking over time
- Automated code fixing through iterative refinement loops
- Session persistence and progress tracking
- Production-ready deployment options (local, Cloud Run, Agent Engine)
- Built-in observability with Cloud Trace integration

## 🌟 Getting Started

1. **Clone this repository**
   ```bash
   git clone https://github.com/chandini2595/Building-e2e-google-adk-agent-applications---using-codelabs.git
   cd Building-e2e-google-adk-agent-applications---using-codelabs
   ```

2. **Choose your project and follow the specific README**
   - For bug management: `cd software_bug_assistant && cat README.md`
   - For development automation: `cd gemini-cli-on-adk && cat README.md`
   - For lead generation: `cd leadGenerationAgentADK && cat README.md`
   - For code review: `cd adk-code-review-assistant && cat README.md`

3. **Set up your environment variables**
   - Get Google API key from [AI Studio](https://aistudio.google.com/apikey)
   - Configure project-specific `.env` files

## 📚 Learning Path

1. **Start with Software Bug Assistant** - Learn ADK basics, database integration, and MCP
2. **Progress to Gemini CLI** - Explore advanced workflows and development automation
3. **Advance to Lead Generation Agent** - Master multi-agent architectures and interactive workflows
4. **Master Code Review Assistant** - Build production-quality systems with dual-pipeline architecture
5. **Deploy to Cloud** - Scale your agents with Google Cloud Run, Agent Engine, and GKE

## 🤝 Contributing

Feel free to contribute improvements, bug fixes, or additional agent examples!

## 📄 License

This project follows the original ADK samples licensing from Google.

---

> **Note**: These are educational samples demonstrating Google ADK capabilities. Adapt the code and configurations for your production use cases.
