# Step 1 of the first demo — run and use the MCP server

Goal: show how to start the MCP server, call a prompt that triggers a tool, and verify data was written.

## Setup and run

1. Open the MCP config (`.vscode/mcp.json`). Explain at a high level:

    - It declares the MCP server (ID/name) and how to start it (command + args).
    - It should point to the Python in your venv and run `src/main.py`.

2. Open the Output view by selecting "More" menu from `mcp.json` and selecting "Show Output".
3. Start or restart the MCP server from the MCP config (click the run button in the editor for `mcp.json`).

    - Goal: show server logs appearing in the Output view.

## Where data lives

4. Open `data/expenses.csv` and note this is the storage location for new entries.

## Try it in GitHub Copilot Chat

5. In Copilot Chat, ensure Agent mode is selected.
6. Click the tools icon and ensure the expenses MCP server/tool is enabled (often named `expenses-mcp`).
7. Type `/` to list commands and pick `/mcp.expenses-mcp.create_expense_prompt`.
8. Provide values for date, amount, category, description, and payment method.
9. Submit the prompt.

- This should invoke the `add_expense` tool and append a row to `data/expenses.csv`.

10. In the same chat, choose `Add Context` → `MCP Resources` → `get_expenses_data` to view the ledger.
11. Re-open `data/expenses.csv` to confirm the new entry was added.

## Quick troubleshooting

- Don’t see slash commands or tools? Ensure the server is running and enabled in Copilot Chat.
- No logs? Check the Output view and that the MCP config points to the correct Python interpreter (see `src/README.md`).
