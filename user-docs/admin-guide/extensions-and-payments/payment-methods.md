# Payment Methods & Gateways

Configure how your store accepts payments and ensure credentials are secured in the hosted environment.

## Supported methods
- Card gateways (as enabled for your tenant)
- Purchase Orders (PO) or manual payments (if allowed by your program)
- Mixed carts with multiple items and quantities

## Configuration
1. Open the store admin and go to the payment configuration area for your gateway(s).
2. Provide live/test credentials as instructed by your team; avoid sharing secrets in documentation.
3. Set per‑store options (currencies, capture vs authorize, order minimums) if available.

## Operational guidance
- Test vs Live: Use test credentials in non‑production and confirm order flows create seats correctly.
- Refunds: Process via the returns/refunds flow so seats and invoice items update consistently.
- Multi‑store: Validate each store’s gateway settings; do not assume global configuration applies to all stores.

## Related
- [Orders & Fulfillment](../orders.md)
- [Discounts & Coupons](discounts-and-coupons.md)
