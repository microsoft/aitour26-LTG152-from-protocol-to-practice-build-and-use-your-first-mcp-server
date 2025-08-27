# Expenses MCP

A simple MCP server that records expense data to CSV and exposes them as a resource. 

## Project purpose

- Demonstrate an MCP server (`src/main.py`) that writes/reads `data/expenses.csv`.
- Provide a reproducible developer setup that avoids interpreter mismatch errors (e.g., `ModuleNotFoundError: No module named 'fastmcp'`).

## Project structure 
/workspace-root/  
- .vscode/  
  - mcp.json  
  - settings.json  
- data/  
  - expenses.csv  
- src/  
  - .venv/             
  - main.py  
  - pyproject.toml  
  - readme.md         

## Prerequisites

- [`uv`](https://docs.astral.sh/uv/getting-started/installation/)
- Python 3.12+

## How to run locally

1. In the terminal move to the src/ directory:
    ```bash
    cd src
    ```

1. Create a vitual environment inside of the `src/` 
    ```bash
    uv venv
    ```

1. Activate the venv:
    ```bash
    source .venv/bin/activate
    ```

1. Install dependencies:
    ```bash
    uv sync
    ```

1. `.vscode/settings.json` should point to the venv you just created:
    ```json
    {
    "python.defaultInterpreterPath": "${workspaceFolder}/src/.venv/bin/python",
    "python.terminal.activateEnvironment": true
    }
    ```

1. Open the command palette (Ctrl+Shift+P) and select "Python: Select Interpreter", then choose the interpreter located at `src/.venv/bin/python`.

1. Open `.vscode/mcp.json` and ensure the `command` points to the venv python:
    ```json
    "command": "${workspaceFolder}/src/.venv/bin/python"
    ```
1. In the same mcp.json file, click run button to start the MCP server.
1. The output view should show the MCP server is running.
1. In GitHub Copilot Chat, make sure you are in Agent mode.
1. In GitHub Copilot Chat, click on the tools icon and ensure the expenses-mcp tool is enabled.
