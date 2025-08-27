# Step 2 of the first demo — walk through the MCP server

Goal: step through the key pieces of the MCP server in `src/main.py` and explain how they work together: prompt → tool → resource.

## What you’ll do
- Open `src/main.py`.
- Follow the flow: Prompt → Tool → Resource.
- Use the talking points below to highlight why each piece is designed this way and how to apply best practices.

---

## 1) Prompt: creating clear instructions for the model
Symbol: `@mcp.prompt def create_expense_prompt(...) -> str`

What it is:
- A function that returns a well-formed instruction string for the model.
- Encodes the exact action to take and the data to use.

Point out:
- Be descriptive and straightforward. The prompt includes all fields (date, amount, category, description, payment method) so nothing is ambiguous.
- It explicitly instructs: “Use the `add_expense` tool to record this transaction.” This removes guesswork and drives the model to the right capability.
- It logs creation so you can trace flows during demos.

Transition: “We’ve told the model what to do. Now let’s see the tool that actually performs the action.”

---

## 2) Tool: the executable capability with types and validation
Symbol: `@mcp.tool async def add_expense(date: str, amount: float, category: str, description: str, payment_method: PaymentMethod)`

What it is:
- A callable operation the model can invoke to perform work (here: append a new row to `data/expenses.csv`).

Point out:
- Clear types keep data explicit (e.g., `float` for amount). The `PaymentMethod` enum (`AMEX`, `VISA`, `CASH`) constrains values and improves reliability.
- Validation is built in: ISO date parsing, positive amount check. Errors are returned as readable strings.
- Logging provides visibility: attempts and failures are recorded via `logger`.
- Persistence details: creates a header row on first write and appends in CSV format. Returns a concise success message.

Transition: “Once data is written, we’ll want a way to expose it back to the model or UI. That’s where resources come in.”

---

## 3) Resource: exposing data in an LLM-friendly format
Symbol: `@mcp.resource("resource://expenses") async def get_expenses_data()`

What it is:
- A read-only endpoint that formats stored data for consumption by the model (and humans).

Point out:
- The resource ID (`resource://expenses`) is a stable handle the client/model can fetch.
- Output is pre-formatted into explicit, labeled lines (Date, Amount, Category, Description, Payment). This structure reduces confusion for LLMs.
- Includes error handling (file not found, generic errors) and logging for observability.

---

## 4) Connect the flow end-to-end
- Prompt collects and clearly states the expense details and explicitly instructs using the `add_expense` tool.
- Tool validates and writes the entry to `data/expenses.csv` with robust typing and logging.
- Resource reads and presents the ledger in a simple, consistent text format that’s easy for the model to summarize or analyze.

---

## 5) Best practices (slide-ready)
- Move back to slides
---

Tip for presenting: use the symbols above to quickly locate each part in `src/main.py`, read 1–2 lines aloud, then summarize the why (not just the what).