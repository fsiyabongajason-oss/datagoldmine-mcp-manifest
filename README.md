# DataGoldMine HFT — MCP Server Manifest

This repository serves as the public metadata manifest for the **DataGoldMine HFT Context Broker**.

* **Server Protocol:** Model Context Protocol (MCP)
* **Live Endpoint:** `https://data-goldbrand.vercel.app/api/v1/mcp`
* **Discovery Card:** `https://data-goldbrand.vercel.app/.well-known/mcp/server-card.json`
* **Payment Protocol:** x402 (USDC on Base)

The primary codebase and automated engine remain hosted securely in a private production repository.

## 🔌 Framework Integrations

### LlamaIndex Integration
```python
import requests

# Fetch DataGoldMine HFT OpenAPI spec directly
spec_url = "[https://data-goldbrand.vercel.app/openapi.json](https://data-goldbrand.vercel.app/openapi.json)"
schema = requests.get(spec_url).json()
print("DataGoldMine HFT Broker active for LlamaIndex pipeline.")

from langchain_community.utilities import OpenAPIWrapper

# Initialize DataGoldMine HFT Node directly via OpenAPI URL
openapi_url = "[https://data-goldbrand.vercel.app/openapi.json](https://data-goldbrand.vercel.app/openapi.json)"
print("DataGoldMine HFT Node active for LangChain Agent.")
