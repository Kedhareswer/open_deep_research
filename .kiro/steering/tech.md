---
inclusion: always
---

# Technology Stack & Standards

## Core Dependencies

- **LangGraph** (>=0.5.4) - Multi-agent workflow orchestration and state management
- **LangChain** - LLM abstraction layer with universal model initialization
- **Python 3.10+** - Minimum version requirement for modern type hints
- **Ruff** - Code formatting and linting with Google docstring style
- **LangSmith** - Experiment tracking and evaluation

## LLM Providers

- **Primary**: OpenAI (GPT-4.1, GPT-5, GPT-4.1-mini, GPT-4.1-nano)
- **Supported**: Anthropic Claude, Google Vertex AI/Gemini, DeepSeek, Groq
- **Requirements**: Must support structured outputs and tool calling
- **Configuration**: Via `init_chat_model()` API for provider flexibility

## Search & Data Sources

- **Primary**: Tavily search API with fallback options
- **Native**: OpenAI and Anthropic web search capabilities
- **MCP Compatible**: Full Model Context Protocol support for extensible tools
- **Additional**: ArXiv, PubMed, DuckDuckGo, Exa, Azure Search

## Development Tools

- **Package Manager**: UV for fast dependency resolution
- **Testing**: Pytest with LangSmith integration
- **Linting**: Ruff with Google docstring convention
- **Type Checking**: MyPy for static type analysis
- **Local Development**: LangGraph CLI with inmem backend

## Deployment Targets

- **Local**: LangGraph dev server on port 2024
- **LangGraph Platform**: Production deployment with authentication
- **Open Agent Platform**: Non-technical user interface
- **Docker**: Containerized deployment support

## Code Quality Standards

- Google docstring style (enforced by ruff)
- Type hints for all function parameters and return values
- Import order: standard library, third-party, local imports
- Error handling with graceful degradation
- Environment variable configuration with validation