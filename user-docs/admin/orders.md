# Orders & Fulfillment

Order management covers payment status, customer requests, and redemption. For mapped products, let the integration control status transitions.

View orders
1) `Sales` → `Orders`.
2) Search and open an order to view details.

Cancellation requests
- Customers can request cancellation before payment is processed. Admins may accept or reject these requests.

Redemption status
- If the product is not auto‑redeem, a `Redeem` link appears on the customer’s Order Details after payment completes.
- Do not manually change order status to `Complete`; it can break the redemption process.

Troubleshooting
- If redemption is blocked by unanswered supplemental questions, the customer should answer them from the Order Details page.
- Use integration logs/webhooks to verify subscription and enrollment updates in NexPort Campus.

