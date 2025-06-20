# Learn LangGraph

⭐ **Star this repository if you find it helpful!**

A project demonstrating how to build conversational AI applications using LangGraph and Anthropic's Claude AI model. This repository contains both simple and advanced examples to help you understand LangGraph's capabilities.

## Overview

This project showcases LangGraph, a library for building stateful, multi-actor applications with LLMs. The tutorial includes two implementations:

1. **Simple Chatbot** - Basic single-node graph implementation
2. **Advanced Chatbot** - Multi-node graph with message classification and routing

Both examples use Claude 3.5 Sonnet to demonstrate different LangGraph patterns and workflows.

## Features

- **Simple Implementation**: Basic chatbot with single-node graph
- **Advanced Implementation**: Multi-agent system with message classification
- **Conditional Routing**: Dynamic routing based on message type (emotional vs logical)
- **Specialized Agents**: Therapist agent for emotional support, logical agent for factual responses
- **State Management**: Conversation flow management across multiple nodes
- **Graph Visualization**: Optional visual representation of graph structure
- **Environment Configuration**: Secure API key management

## Prerequisites

- Python 3.12 or higher
- Anthropic API key

## Installation

1. Clone the repository:

```bash
git clone https://github.com/asheint/learn-langgraph.git
cd learn-langgraph
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

### Simple Chatbot

Run the basic single-node chatbot:

```bash
python simple.py
```

This implementation demonstrates:

- Basic state definition with message handling
- Single-node graph structure
- Simple message flow: START → chatbot → END

### Advanced Chatbot

Run the multi-agent chatbot with message classification:

```bash
python advanced.py
```

This implementation demonstrates:

- Message classification using structured output
- Conditional routing based on message type
- Specialized agents (therapist vs logical)
- Complex graph flow with multiple decision points

Type `exit` to quit the advanced chatbot.

## Project Structure

```
├── simple.py           # Basic single-node chatbot implementation
├── advanced.py         # Multi-agent chatbot with classification
├── pyproject.toml      # Project configuration and dependencies
├── .env               # Environment variables (create this file)
├── .python-version    # Python version specification
└── README.md          # This file
```

## How It Works

### Simple Implementation (simple.py)

1. **State Definition**: State class with message list using `add_messages`
2. **Single Node**: `chatbot` function processes all messages
3. **Linear Flow**: START → chatbot → END
4. **Direct Response**: User input → Claude response

### Advanced Implementation (advanced.py)

1. **Enhanced State**: State class with message classification
2. **Message Classification**: `classify_message` categorizes input as emotional or logical
3. **Conditional Routing**: `router` directs to appropriate agent
4. **Specialized Agents**:
   - `therapist_agent`: Provides emotional support and empathy
   - `logical_agent`: Delivers factual, logic-based responses
5. **Complex Flow**: START → classifier → router → (therapist|logical) → END

## Key Components

- **LangGraph**: Graph-based workflow framework for multi-step AI applications
- **LangChain**: Chat model initialization and message management
- **Anthropic Claude**: Underlying AI model for generating responses
- **Pydantic**: Structured output for message classification
- **State Management**: Conversation context preservation across nodes

## Dependencies

- `langgraph>=0.4.8` - Graph-based workflow framework
- `langchain[anthropic]>=0.3.25` - LangChain with Anthropic integration
- `python-dotenv>=1.1.0` - Environment variable management
- `ipykernel>=6.29.5` - Jupyter notebook support for graph visualization

## Graph Visualization

Both implementations include optional graph visualization. When run in a Jupyter notebook, they can display visual representations of the graph structures using Mermaid diagrams.

## Learning Path

1. **Start with simple.py**: Understand basic LangGraph concepts
2. **Progress to advanced.py**: Learn multi-node graphs and conditional routing
3. **Experiment**: Modify the classification logic or add new agent types
4. **Extend**: Add memory, tool usage, or more complex routing logic

## Examples

### Simple Chatbot Interaction

```
Enter a message: What is the capital of France?
Paris is the capital of France.
```

### Advanced Chatbot Interactions

**Logical Query:**

```
Message: What is the capital of France?
Assistant: Paris is the capital of France. It is located in the north-central part of the country...
```

**Emotional Query:**

```
Message: I'm feeling really stressed about work lately
Assistant: I hear that you're feeling stressed about work, and I want you to know that what you're experiencing is completely valid...
```

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

**Repository**: [https://github.com/asheint/learn-langgraph](https://github.com/asheint/learn-langgraph)

⭐ **Star this repository if you find it helpful!**
