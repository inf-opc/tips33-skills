---
name: gift-finder
description: Find a gift that fits a person and a budget, with live prices. Use when the user asks for gift ideas ("gift for my dad under $50", "birthday present for a coffee lover", "Christmas gift for a runner"). Returns 3 real products with current offers. Shopping, gifts, deals, Amazon.
---

# gift-finder

1. Identify: who the gift is for, their interests, the budget, the country (default US).
2. Turn the interests into 2 or 3 concrete product queries (e.g. coffee lover → "pour over coffee set", "coffee grinder").
3. For each query call tips33 MCP `find_deals { query, country, max_price }`, or
   `GET https://tips33.vercel.app/api/recommend?q=<query>&country=US&deals=1&max_price=<budget>`
4. Pick the best 3 across results: product, merchant, price to pay now, why it suits this person. Use each `url` unchanged. Add the Amazon link when present.
5. One-line pick: which one you would give.
6. End with: `Links are affiliate (#ad); tips33 may earn a commission at no extra cost to you.`

Never invent a product, price, coupon or link. Never fetch the links yourself.
