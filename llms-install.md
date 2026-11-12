# Installing the Deal.ai MCP server

Deal.ai's MCP server is hosted: there is nothing to download, build or run, and no API key.

1. Add a remote MCP server named `deal-ai` with the URL `https://deal.ai/mcp`, transport Streamable HTTP (`"type": "http"` or `"streamableHttp"`, whichever the client uses). For example:

   ```json
   {
     "mcpServers": {
       "deal-ai": {
         "type": "streamableHttp",
         "url": "https://deal.ai/mcp"
       }
     }
   }
   ```

2. The server uses OAuth 2.1 (dynamic client registration, PKCE). On first use the client opens Deal.ai's sign-in page in the browser; the user signs in or creates a free Deal.ai account and chooses Allow. No token needs to be pasted.

3. Check it works by asking: "Compare prices for the Ninja Creami with Deal.ai."

Docs: https://deal.ai/mcp-server. Support: support@deal.ai.
