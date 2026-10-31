# LLM-Evaluation
Used for LLM Evaluation
# Tool-Calling AI Agent

An AI agent that uses Large Language Models (LLMs) to understand user requests, select appropriate tools, execute actions, and generate responses based on tool outputs.

## Overview

This project demonstrates how to build a tool-calling AI agent that can go beyond text generation by interacting with external tools.

Instead of relying only on an LLM's internal knowledge, the agent identifies when a tool is needed, invokes the appropriate function, processes the result, and returns a useful response.

## Key Features

- **LLM-based reasoning:** Understands user instructions and determines the next action.
- **Tool selection:** Chooses relevant tools based on the user's request.
- **Function calling:** Executes registered Python functions.
- **Tool result handling:** Processes tool outputs and incorporates them into the final response.
- **Multi-step execution:** Supports workflows involving multiple tool calls.
- **Error handling:** Handles invalid tool requests and execution failures.
- **Modular architecture:** Allows new tools to be added easily.

## Architecture

```text
             User Query
                 |
                 v
          AI Agent / LLM
                 |
          Analyze Request
                 |
                 v
          Select Tool(s)
                 |
                 v
          Execute Function
                 |
                 v
          Tool Result
                 |
                 v
        LLM Processes Result
                 |
                 v
          Final Response
```

## Technology Stack

- Python
- Large Language Models (LLMs)
- LLM function/tool calling
- REST APIs (if integrated)
- Pydantic (if used for validation)
- Pytest
- Git and GitHub

## Project Structure

```text
tool-calling-ai-agent/
│
├── src/
│   ├── agent.py
│   ├── tools.py
│   ├── tool_registry.py
│   └── config.py
│
├── tests/
│   └── test_agent.py
│
├── examples/
│   └── example_usage.py
│
├── requirements.txt
├── .env.example
├── .gitignore
├── LICENSE
└── README.md
```

*The structure above is illustrative; adjust it to match the actual repository.*

## Installation

Clone the repository:

```bash
git clone https://github.com/Chanikyaa/tool-calling-ai-agent.git
cd tool-calling-ai-agent
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it:

**Windows**
```bash
.venv\Scripts\activate
```

**Linux / macOS**
```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Configuration

Create a `.env` file based on `.env.example` and add the API key required by your selected LLM provider.

```env
LLM_API_KEY=your_api_key_here
```

Never commit API keys or secrets to GitHub.

## Usage

After implementation, run the agent using the entry point provided by the project.

For example:

```bash
python -m src.agent
```

Example interaction (illustrative):

```text
User: What is 25 multiplied by 16?

Agent: I'll use the calculator tool.

Tool Output: 400

Agent: 25 multiplied by 16 is 400.
```

## Testing

Run the test suite:

```bash
pytest
```

## Engineering Concepts Demonstrated

- Agentic AI workflows
- LLM tool/function calling
- Structured input and output
- Tool registration and execution
- Multi-step reasoning
- Exception handling
- Modular Python application design
- Unit testing

## Future Improvements

- Add support for multiple LLM providers.
- Integrate web search and database tools.
- Add memory for multi-turn conversations.
- Implement tool execution limits and timeouts.
- Add tracing and observability.
- Deploy the agent through a REST API.

## Author

**Palli Chanikya Paidi Balaji**

B.Tech – VIT Chennai (2025)  
M.Tech CSE – AI & Data Science, Mahindra University (2026–2028)

GitHub: [@Chanikyaa](https://github.com/Chanikyaa)

---

*This project is part of an AI/ML Engineering Portfolio focused on practical AI systems and production-oriented development.*
