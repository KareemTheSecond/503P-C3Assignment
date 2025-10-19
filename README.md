# The House of Candy — Conversational Agent

This system is an assisant that acts as the whimsical candy concierge (helper...) for *The House of Candy*, a fictional company that transforms homes into fully edible candy masterpieces using its magical “dip-dip” chocolate cauldron.

---

## What It Does

The system uses **OpenAI’s function calling** (`tools`) to process user requests, automatically calling internal functions to:
- **Record customer interest** when users share their name, email, and a message.
- **Record feedback** whenever the assistant cannot answer a question (for follow-up by a “chocolatier”).
- **Calculate candy pricing** for home transformations or sales using fixed company rules.

All interactions, including tool calls and model responses, are logged into JSONL files for review and traceability.

---

## Tools Implemented

| Tool Name | Purpose | Output Log |
|------------|----------|------------|
| `record_customer_interest` | Stores user leads (name, email, message) in `logs/customer_interest.jsonl`  |
| `record_feedback` | Captures unanswerable or out-of-scope questions in `logs/feedback.jsonl`  |
| `calculate_candy_price` | Computes a quote based on the home’s value and mode (“transform” or “sell”)  |

---



## Output Files

All logs are automatically created in the `/logs` directory:

