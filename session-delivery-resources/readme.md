## How to deliver this session

🥇 Thanks for delivering this session!

Prior to delivering the workshop please:

1.  Read this document and all included resources included in their entirety.
2.  Watch the video presentation
3.  Ask questions of the content leads! We're here to help!


## 📁 File Summary

| Resource | Link | Description |
|---|---|---|
| Demos | [../docs/01-demo/](../docs/01-demo/) | Step-by-step guides for Demo 1 and Demo 2. |
| Docs | [../docs/README.md](../docs/README.md) | Presenter-facing overview and pointers. |
| Server Code | [../src/main.py](../src/main.py) | Minimal MCP server implementation. |
| Train‑the‑Trainer Video | https://aka.ms/tbd-train-video | Recording for presenters (placeholder). |
| Slide Deck | https://aka.ms/tbd-slide-deck | Slide deck for presenters (placeholder). |


## 🚀 Get Started

This is a 15‑minute talk with two short demos (no labs).

### 🕐 Timing (15 minutes)

| Time | Segment |
|---|---|
| 0:00 – 2:00 | Slides: What is MCP? Hosts, clients, servers; prompts, tools, resources. |
| 2:00 – 6:00 | Demo 1: Use the server in VS Code (prompt → tool → resource). |
| 6:00 – 12:00 | Demo 2: Code tour in `src/main.py` (types, enums, validation, logging). |
| 12:00 – 15:00 | Slides: Best practices and conclusion. |

### 🏋️ Preparation
- Ensure Python 3.12+, `uv`, and dependencies are installed (see `../src/README.md`).
- Use the provided `.vscode/mcp.json` to start the MCP server with the venv interpreter; open the Output view.
- Verify `data/expenses.csv` exists (it’s provided in the repo) and note this is the ledger file that will be appended to.
- In GitHub Copilot Chat (VS Code): enable Agent mode and the expenses MCP tool.
- Sanity check: run the prompt to add a small test expense and confirm it appears in the resource and CSV.

### 🖥️ Demos
Demo 1 (How to use it) — 4 minutes
- Follow: ../docs/01-demo/01-step.md
- In Copilot Chat: run the `create_expense_prompt`, which invokes `add_expense`, then fetch `get_expenses_data`.
- Show `data/expenses.csv` updated and logs in Output.

Demo 2 (How it works) — 6 minutes
- Follow: ../docs/01-demo/02-step.md
- In `src/main.py`: walk Prompt → Tool → Resource.
	- Prompt: clear instruction that explicitly calls `add_expense`.
	- Tool: typed params, `PaymentMethod` enum, validation, logging, CSV write.
	- Resource: formatted, labeled lines for LLMs; error handling and logging.
