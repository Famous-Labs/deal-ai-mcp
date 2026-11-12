---
name: deal-ai-shopping
description: Use when the user asks what to buy, where a product is cheapest, whether a price or deal is good, for a product's price history, or to be told when a price drops. Uses the Deal.ai MCP server's tools.
---

# Shopping with Deal.ai

## When to use

The user wants a product recommendation, a price comparison across stores, a check of a price or a product link, price history, or a price alert.

## Instructions

1. Recommendations ("best X under $Y"): call `ask_deal_ai` with the request, then call `get_deal_ai_answer` with the returned `search_id`. If it says the agent is still working, wait about 20 seconds and call it again. Follow-up questions go to `ask_deal_ai` with the same `search_id`.
2. Checking a price or a product link: call `check_deal`, then `get_deal_check` for the verdict and each store's price.
3. One product's prices across stores and its price history: `get_product_prices`. Specs and details: `get_product_details`. Two to four products side by side: `compare_products`. Current deals: `get_deals`. Anything else on Deal.ai: `search_products`.
4. Price alerts: `watch_price`, `list_watched`, `stop_watching`.
5. Give the user the Deal.ai page link and the store links each answer includes. Prices are listed prices at the time shown, before tax.

The first tool call opens Deal.ai's sign-in in the browser (a free account, no API key).
