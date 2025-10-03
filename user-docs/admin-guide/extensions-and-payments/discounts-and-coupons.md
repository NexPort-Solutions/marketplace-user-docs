# Discounts & Coupons

Configure and manage price incentives while preserving accurate seat creation and mapping behavior.

## Concepts
- Exclusive vs cumulative: Choose the highest applicable discount or allow stacking.
- Usage limits: Restrict by customer (e.g., N times per customer) and by date range.
- Scope: Apply to products, categories, or the whole cart; ensure category‑level rules align with single‑item‑per‑category settings if used.

## Setup
1. Create a discount with name, type, and discount amount/percentage.
2. Set exclusivity and usage limits.
3. Add a coupon code (promo code) if required and set validity windows.
4. Assign the discount to products/categories as needed.

## Behavior with seats
- Discounts change price only. Seat creation still matches product quantity on the order.
- Open‑ended products and mappings behave the same; redemption mode is unaffected by discounts.

## Tips
- Communicate stackability rules to customers to avoid confusion.
- For organization purchases, validate that bulk discounts do not conflict with assignment flows.

## Related
- [Products](../products.md)
- [Orders & Fulfillment](../orders.md)
