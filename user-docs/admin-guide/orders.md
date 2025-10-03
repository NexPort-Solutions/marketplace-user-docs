# Orders & Fulfillment

Use the Orders area to search, review, and act on purchases. In <code class="expression">space.vars.PRODUCT_NAME</code>, mapped products create seats/enrollments in NexPort Campus. Let the integration drive status changes; avoid forcing manual order status transitions.

## View and search orders
1) Go to `Sales` → `Orders`.
2) Use filters to narrow results, then open an order to view details.

Common filters
- Date range, Store, Payment status, Order status, Shipping status
- Product (by name), Billing email/phone/last name, Payment method
- Vendor or Warehouse (if applicable in your tenant)

> Tip: Export found or selected orders to Excel/XML from the Orders list as needed.

## Order details

### Info
- Order #: Unique order number; Created on; Customer.
- Order status: Pending, Processing, Complete, Cancelled.
  - Do not set to Complete manually for mapped items; completion is driven by payment + fulfillment and can impact redemption.
- Payment status: Pending, Authorized, Paid, Partially refunded, Refunded, Voided.
  - Authorized: buttons to `Capture` or `Void` may be available depending on gateway.
  - Paid: `Refund` or `Partial refund` actions are available; see Returns & Refunds for how seats are reclaimed.
- Totals: Subtotal, Shipping, Tax, Total, Profit; `Edit order totals` when corrections are required (rare for mapped digital items).

### Billing & shipping
- Billing and Shipping addresses; Shipping method; Shipping status.
- Shipments list and `Add shipment` apply to physical goods. Mapped NexPort products are digital and do not require shipping.

### Products
- Shows each line item with price, quantity, and total. You can add or remove products and edit quantities.
- For mapped NexPort items:
  - Changing quantities or removing lines after payment can desynchronize seats. Prefer using the seats workflow (assign, unassign/return) instead of editing the product list.
  - Downloadable license/upload actions do not apply; fulfillment occurs via seat creation in NexPort Campus.

### Order notes
- Add internal notes (optionally visible to the customer) and attach files. Notes are useful for documenting return/assignment decisions.

## Marketplace‑specific behaviors

Mapped (training) products create entitlements in NexPort Campus. The following additions apply:

- Redemption mode
  - Auto‑redeem: Enrollment is created automatically after payment is captured; no manual Redeem action needed.
  - Manual redeem: The purchaser sees a `Redeem` link on Order Details; admins can Assign a seat directly from the order.
- Seats lifecycle
  - Assign: Attach an available seat to a learner; creates the enrollment.
  - Email redemption: Sends a link and moves the seat to Awaiting; cancel to reclaim the seat.
  - Unassign/Return: Reclaims the seat; see Returns & Refunds for refund behavior.
- Supplemental info holds
  - If supplemental questions are required, the purchaser or recipient must answer them before redemption completes.
- Status control
  - Avoid manually forcing `Complete`. The integration updates statuses as payment, redemption, and returns occur.

## Cancellation and return requests
- Customers can request cancellation/return according to store policy. Admins approve or deny from the order or return‑requests list.
- Approved returns for mapped items reclaim seats and update invoice item statuses; see Returns & Refunds for details.

## Troubleshooting
- No Redeem/Assign available: Confirm mapping exists and the order is Paid; check for supplemental info requirements.
- Seat won’t unassign due to existing enrollment: Resolve the learner’s existing enrollment state per policy, then retry.
- Status looks wrong after a refund: Reopen the order to refresh; if still incorrect, review payment gateway logs and retry supported actions.

## Shipping management
- Shipping applies only to physical goods. Mapped NexPort items are digital and set Shipping not required.
- Shipping statuses you may see on mixed orders:
  - Shipping not required: Digital-only lines (e.g., mapped training).
  - Not yet shipped → Partially shipped → Shipped → Delivered: Progression for physical items as shipments are created and completed.
- Use `Add shipment` for physical lines; include tracking numbers and mark Shipped/Delivered as appropriate. Do not create shipments for mapped training lines.

## Inventory and stock
- Mapped training products usually do not track stock. Use “Don’t track inventory” for these items.
- Physical products can use standard inventory tracking.
- Open‑ended selector products should not track inventory; track inventory at the underlying fixed products if needed.
- Avoid adjusting quantities post‑payment on mapped items; manage availability via seats (assign/unassign/return) instead.

## Order settings (hosted‑safe subset)
- Returns and refunds: Enabled per store policy to support reclaiming seats for mapped items.
- PDF invoices and notifications: Can be enabled; these do not impact redemption.
- Payment capture: Some gateways authorize at checkout and capture later. Seat creation occurs after capture when Auto‑redeem is enabled.
- Checkout guest/anonymous: Typically disabled for B2B training flows; confirm with your tenant configuration.
> Note: Some settings are centrally managed in hosted environments. Contact support before changing global order settings.

## Checkout attributes vs Supplemental Info
- Checkout attributes collect extra data during checkout (applies to the order as a whole).
- Supplemental Info (Marketplace feature) collects data at seat/redeem time and can drive group membership or mapping behavior.
- Guidance:
  - Prefer Supplemental Info for learner‑specific questions required for enrollment.
  - Use checkout attributes for order‑level metadata that doesn’t affect mapping (e.g., internal PO number).

## Status reference (quick)
- Order status: Pending, Processing, Complete, Cancelled.
  - For mapped items, do not force Complete manually.
- Payment status: Pending, Authorized, Paid, Partially refunded, Refunded, Voided.
  - Authorized → Capture to settle funds; Paid enables Refund/Partial refund.
- Shipping status: Shipping not required, Not yet shipped, Partially shipped, Shipped, Delivered.
  - Digital mapped items report Shipping not required.

## Related
- [Assigning and Transferring NexPort Campus Seats](assigning-and-transferring-seats/README.md)
- [Email Redemption Links for Seats](email-redemption-links-for-seats.md)
- [Returns and Refunds for Seats](returns-and-refunds-for-seats.md)
- [NexPort Mapping](nexport-mapping.md)
