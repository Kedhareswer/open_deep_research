---
inclusion: always
---

# Project Structure Guidelines

## Core Architecture Files

- `src/open_deep_research/deep_researcher.py` - Main LangGraph implementation and entry point
- `src/open_deep_research/state.py` - Typed state classes for LangGraph state management
- `src/open_deep_research/configuration.py` - Centralized configuration management
- `src/open_deep_research/prompts.py` - All system prompts and templates
- `src/open_deep_research/utils.py` - Utility functions and helpers

## Configuration & Deployment

- `langgraph.json` - LangGraph platform configuration and graph definitions
- `pyproject.toml` - Python project configuration, dependencies, and build settings
- `.env.example` - Environment variable template for API keys and settings
- `src/security/auth.py` - Authentication handling for deployments

## Testing & Evaluation

- `tests/run_evaluate.py` - Main evaluation script for Deep Research Bench
- `tests/extract_langsmith_data.py` - LangSmith experiment data extraction
- `tests/evaluators.py` - Custom evaluation logic and metrics
- `tests/pairwise_evaluation.py` - Comparative evaluation tools

## Legacy Implementations

- `src/legacy/` - Previous implementations for reference and comparison
  - Contains alternative architectural approaches
  - Maintained for backward compatibility and learning
  - Less performant but demonstrates different design patterns

## Key Patterns

- **Single Entry Point**: All functionality accessible through `deep_researcher.py`
- **Centralized Config**: All settings managed in `configuration.py`
- **Typed State**: Immutable state management through typed classes
- **Modular Prompts**: Separated prompt templates for maintainability
- **Test-Driven**: Comprehensive evaluation framework with benchmarking
