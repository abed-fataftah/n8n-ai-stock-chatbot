# AI Stock Chatbot

An n8n chat workflow that connects an AI agent to Marketstack end-of-day stock data, with conversation memory and an OpenAI chat model.

## How it works

1. A chat message starts the workflow.
2. The AI agent uses OpenAI (`gpt-5-mini`) to process the request.
3. Simple Memory provides conversation context.
4. When needed, the agent calls Marketstack with a stock ticker to retrieve the latest available end-of-day data.
5. The agent responds in the chat.

This workflow retrieves end-of-day data, not a real-time price feed.

## Setup

1. Download `workflow.json` from this repository.
2. In n8n, create a workflow and choose **Import from File** from the workflow menu.
3. Select `workflow.json`.
4. Open **OpenAI Chat Model** and select or create your OpenAI API credential.
5. Open **Get many EoD data in Marketstack** and select or create your Marketstack API credential.
6. Confirm that the selected OpenAI model and Marketstack operation are available for your accounts.
7. Save the workflow, open its chat, and send a test message.

Example: `Get the latest available end-of-day stock data for AAPL.`

## Files

- `workflow.json` — importable n8n workflow, inactive by default.
- `README.md` — overview and setup instructions.

## Credentials and validation

Account-specific credential references and instance metadata have been removed from the shared export. Configure your own credentials inside n8n; do not commit API keys.

The JSON structure was checked before upload. Execution requires your n8n instance and configured credentials and has not been tested from this repository.
