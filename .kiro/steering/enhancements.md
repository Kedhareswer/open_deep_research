---
inclusion: always
---

# Open Deep Research Development Guidelines

## Architecture Patterns

### LangGraph State Management

- Use typed state classes in `state.py` for all graph state definitions
- Maintain immutable state updates through proper state transitions
- Follow the supervisor-researcher multi-agent pattern for parallel processing

### Model Configuration

- Support multiple LLM providers via `init_chat_model()` API
- Separate models by task: summarization, research, compression, final reporting
- Ensure all models support structured outputs and tool calling
- Default to OpenAI models but maintain provider flexibility

### Search Integration

- Default to Tavily search API with fallback options
- Support MCP-compatible search tools
- Implement native web search for Anthropic and OpenAI when available
- Handle search result summarization and compression consistently

## Code Style & Standards

### Python Conventions

- Follow Google docstring style (enforced by ruff)
- Use type hints for all function parameters and return values
- Maintain Python 3.10+ compatibility
- Structure imports: standard library, third-party, local imports

### Error Handling

- Implement graceful degradation for API failures
- Log errors with appropriate context for debugging
- Provide meaningful error messages for configuration issues
- Handle rate limiting and timeout scenarios

### Configuration Management

- Use environment variables for API keys and sensitive data
- Centralize configuration in `configuration.py`
- Support both local development and production deployment configs
- Validate configuration at startup

## Testing & Evaluation

### Evaluation Framework

- Use Deep Research Bench for performance benchmarking
- Target RACE score improvements through systematic testing
- Cost-aware evaluation (track token usage and API costs)
- Support both English and Chinese research tasks

### Test Structure

- Place evaluation scripts in `tests/` directory
- Use LangSmith for experiment tracking and comparison
- Generate JSONL output compatible with Deep Research Bench
- Include pairwise evaluation capabilities

## Deployment Considerations

### LangGraph Platform

- Maintain compatibility with LangGraph Studio UI
- Support local development server on port 2024
- Ensure proper graph definition in `langgraph.json`
- Handle authentication through `src/security/auth.py`

### Performance Optimization

- Implement parallel processing for multiple researchers
- Use appropriate model selection for cost/quality tradeoffs
- Cache search results when appropriate
- Monitor token usage across different model configurations

## Security & Best Practices

### API Key Management

- Never commit API keys to version control
- Use `.env` files for local development
- Support multiple provider authentication methods
- Validate API key presence before execution

### Data Handling

- Sanitize and validate all external search results
- Implement proper content filtering for research sources
- Handle large document processing efficiently
- Respect rate limits and usage quotas

## Legacy Code Management

### Backward Compatibility

- Maintain legacy implementations in `src/legacy/` for reference
- Document performance differences between implementations
- Preserve alternative architectural approaches
- Keep legacy code functional but clearly marked as deprecated
