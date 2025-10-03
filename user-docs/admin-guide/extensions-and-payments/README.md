# Extensions & Payments

This section covers payment methods, discounts and coupons, currencies and taxes, and enrollment extensions in <code class="expression">space.vars.PRODUCT_NAME</code>. It focuses on hosted configuration and how each area interacts with product mappings and seats.

## Overview
- Payment methods: Cards, purchase orders, manual payments (as enabled by your store). Configure securely per store.
- Discounts & coupons: Exclusive vs cumulative, usage limits per customer, scheduling, and scope.
- Currencies & taxes: Base/store currency settings and optional tax rules (if enabled for your program).
- Enrollment extensions: Products and mappings that extend existing enrollments with approval options and thresholds.

## How this relates to seats and orders
- Payments complete an order and create seats for mapped products. Refunds are handled in the returns/refunds flow and update seat availability.
- Discounts change the price but not the mapping; seats are still created based on product quantity.
- Extensions are special products that extend existing enrollments instead of creating new ones.

## Topics
- Payment Methods & Gateways
- Discounts & Coupons
- Currencies & Taxes
- Enrollment Extensions
- Exports & Statements

## Related
- [Orders & Fulfillment](../orders.md)
- [NexPort Mapping](../nexport-mapping.md)
