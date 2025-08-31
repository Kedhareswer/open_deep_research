---
inclusion: always
---

# Open Deep Research Product Overview

Open Deep Research is a configurable, fully open-source deep research agent that performs PhD-level research tasks across multiple domains. The system conducts comprehensive research by planning and executing multi-step research workflows, searching across various APIs, synthesizing findings from multiple sources, and generating structured, academic-quality reports.

## Core Architecture

- **Multi-Agent System**: Supervisor-researcher coordination with parallel processing
- **LangGraph-Based**: Built on LangGraph framework with typed state management
- **Model Agnostic**: Supports multiple LLM providers (OpenAI, Anthropic, Google, etc.)
- **Search Integration**: Tavily, native web search, MCP-compatible search tools
- **Task Specialization**: Separate models for summarization, research, compression, and final reporting

## Key Features

- **MCP Integration**: Full Model Context Protocol compatibility for extensible tool integration
- **Evaluation Framework**: Benchmarked against Deep Research Bench with RACE scoring (currently #6 with 0.4344 score)
- **Production Ready**: Deployable on LangGraph Platform, Open Agent Platform, and local development
- **Cost Optimization**: Configurable model selection for cost/quality tradeoffs
- **Multi-Language**: Supports both English and Chinese research tasks

## Performance Expectations

- PhD-level research quality across 22 domains
- Parallel processing for faster report generation
- Cost-aware evaluation with token usage tracking
- Academic-quality structured output with proper citations