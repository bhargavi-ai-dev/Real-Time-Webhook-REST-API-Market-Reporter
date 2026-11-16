# Real-Time Webhook & REST API Market Reporter (n8n)

An event-driven AI pipeline built in **n8n** that triggers via a custom **Webhook**, fetches live market JSON data using an **HTTP GET Request**, and generates investor summaries using an **LLM**.

## Architecture
1. **Webhook Trigger:** Listens for incoming HTTP requests to initiate the workflow.
2. **REST API Integration:** Connects to the public Coinbase API (`GET /v2/prices/BTC-INR/spot`) without pre-built plugins to extract live pricing JSON.
3. **AI Summarization:** Passes dynamic JSON variables into an LLM chain to generate concise financial updates.
