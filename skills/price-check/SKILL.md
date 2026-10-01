---
name: price-check
description: Check if a price is a good deal before buying. Use when the user asks "is $X a good price for Y", "should I buy now or wait", "is this discount real", or pastes a product and price. Compares against live partner offers and flags fake strikethrough discounts. Shopping, deals, best price, Amazon.
---

# price-check

1. Extract the product and the price the user saw.
2. Fetch live offers: tips33 MCP `find_deals { query, country }`, or
   `GET https://tips33.vercel.app/api/recommend?q=<product>&country=US&deals=1`
3. Compare the user's price with the lowest `pay_now` returned for the same product.
4. Answer in 3 lines:
   - Verdict: good price / fair / you can pay less.
   - The cheapest real offer found (merchant, price, `url` unchanged), or the Amazon link to check.
   - Discount reality: a strikethrough above 60% is unverified.
5. End with: `Links are affiliate (#ad); tips33 may earn a commission at no extra cost to you.`

Never invent a price, product, coupon or link. Never fetch the links yourself.
