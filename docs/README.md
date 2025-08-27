# From Protocol to Practice: Build and Use Your First MCP Server — Docs

## Introduction
This folder contains the presenter-facing guides for the live demos that showcase a minimal MCP server which records expenses to CSV and exposes them as a resource. Use these steps to run the server, invoke a prompt that calls a tool, and verify results.

## Quick start (presenters)
1. Complete local setup in the developer guide: see `src/README.md` (venv, dependencies, interpreter).
2. Open `.vscode/mcp.json` and start the MCP server (use the Run button in the editor).
3. Open the Output view to watch logs from the server.
4. Confirm the ledger path: `data/expenses.csv`.

## Demos
- Step 1: Run and use the MCP server
	- Walk through starting the server, using the prompt via Copilot Chat, and verifying the CSV.
	- Guide: `01-demo/01-step.md`

- Step 2: Tour the code (prompt → tool → resource)
	- Explain how each part is implemented in `src/main.py` and why it’s structured that way.
	- Guide: `01-demo/02-step.md`

## Key endpoints and names
- Prompt: `create_expense_prompt` (slash command: `/mcp.expenses-mcp.create_expense_prompt`)
- Tool: `add_expense(date, amount, category, description, payment_method)`
	- `payment_method` is an enum: `AMEX`, `VISA`, `CASH`
- Resource: `resource://expenses` → `get_expenses_data`

## Troubleshooting
- Tools not visible in Copilot Chat? Ensure the MCP server is running and enabled in the tools list.
- No logs? Start from `.vscode/mcp.json` and verify the Python interpreter points to `src/.venv/bin/python` (see `src/README.md`).


