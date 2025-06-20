# LangGraph Tutorial

A beginner-friendly tutorial project demonstrating how to build conversational AI applications using LangGraph and Anthropic's Claude AI model.

## Overview

This project showcases the basics of LangGraph, a library for building stateful, multi-actor applications with LLMs. The tutorial implements a simple chatbot that uses Claude 3.5 Sonnet to respond to user messages through a graph-based workflow.

## Features

- Simple chatbot implementation using LangGraph
- Integration with Anthropic's Claude 3.5 Sonnet model
- State management for conversation flow
- Graph visualization capabilities
- Environment variable configuration for API keys

## Prerequisites

- Python 3.12 or higher
- Anthropic API key

## Installation

1. Clone the repository:

```bash
git clone https://github.com/asheint/langgraph-tutorial.git
cd langgraph-tutorial
```

2. Create a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. Install dependencies using uv (recommended) or pip:

```bash
# Using uv
uv sync

# Or using pip
pip install -r requirements.txt
```

4. Create a `.env` file in the project root and add your Anthropic API key:

```
ANTHROPIC_API_KEY=your_api_key_here
```

## Usage

Run the chatbot:

```bash
python main.py
```

Enter your message when prompted, and the chatbot will respond using Claude 3.5 Sonnet.

## Project Structure

```
├── main.py              # Main chatbot implementation
├── pyproject.toml       # Project configuration and dependencies
├── .env                 # Environment variables (create this file)
├── .python-version      # Python version specification
└── README.md           # This file
```

## How It Works

1. **State Definition**: The `State` class defines the conversation state using TypedDict with message handling
2. **Graph Building**: A StateGraph is created with a single "chatbot" node
3. **Node Function**: The `chatbot` function processes messages using the Claude model
4. **Graph Execution**: Messages flow from START → chatbot → END
5. **Response**: The latest AI response is displayed to the user

## Key Components

- **LangGraph**: Provides the graph-based workflow framework
- **LangChain**: Handles the chat model initialization and message management
- **Anthropic Claude**: The underlying AI model for generating responses
- **State Management**: Maintains conversation context through the graph execution

## Dependencies

- `langgraph>=0.4.8` - Graph-based workflow framework
- `langchain[anthropic]>=0.3.25` - LangChain with Anthropic integration
- `python-dotenv>=1.1.0` - Environment variable management
- `ipykernel>=6.29.5` - Jupyter notebook support for graph visualization

## Graph Visualization

The project includes optional graph visualization capabilities. When run in a Jupyter notebook, it can display a visual representation of the graph structure.

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## Support

If you found this tutorial helpful, consider buying me a coffee:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/asheint)

## License

This project is open source and available under the MIT License.

## Learn More

- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [LangChain Documentation](https://python.langchain.com/)
- [Anthropic API Documentation](https://docs.anthropic.com/)

---

**Repository**: [https://github.com/asheint/langgraph-tutorial](https://github.com/asheint/langgraph-tutorial)
