# Deal.ai

Use the `deal-ai` MCP server's tools for shopping questions: what to buy, where a product is cheapest, whether a price or deal is good, price history, and price alerts.

- To recommend products, call `ask_deal_ai`, then `get_deal_ai_answer` until the answer is ready.
- To check a price or a product link, call `check_deal`, then `get_deal_check`.
- For one product's prices across stores, use `get_product_prices`; for side-by-side, `compare_products`; for current deals, `get_deals`.
- Give the shopper the Deal.ai page link and the store links each answer includes. Prices are listed prices at the time shown, before tax.

The first call opens Deal.ai's sign-in in the browser (free account, no API key).
