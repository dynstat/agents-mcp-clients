# MCP File Operations Agent

A simple Model Context Protocol (MCP) implementation providing file system operations through a server-client architecture.

## Components

- **file_agent_server.py**: MCP server exposing file system operations as tools
- **file_agent_client.py**: Client implementation using Google's Gemini API

## Features

- Read file contents
- Write content to files
- List directory contents

## Requirements

- Python ≥3.12
- `mcp[cli]>=1.6.0`
- `google-genai>=1.12.1`

## Setup

1. Install dependencies: `pip install -e .`
2. Create a `.env` file with your API keys (see `.env-sample`)
3. Run server: `python file_agent_server.py`
4. Run client: `python file_agent_client.py`

## Cursor IDE Integration

Configure in `.cursor/mcp.json`:
```json
{
  "mcpServers": {
    "File Operations Agent": {
      "command": "python",
      "args": ["path/to/file_agent_server.py"],
      "env": {}
    }
  }
}
```