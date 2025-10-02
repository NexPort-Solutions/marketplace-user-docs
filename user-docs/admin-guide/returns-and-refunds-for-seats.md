# Returns and Refunds for Seats

Use returns and refunds when an organization needs to reclaim a seat from a purchase. This page covers return requests, status changes, and how refunds affect seats and enrollments.

## Overview
- Scope: Seats from organization purchases managed by purchasing agents or admins.
- Outcomes: Returned seats go back to “Available” and can be reassigned; refunds update order and invoice item statuses.
- Roles: Customers (purchasing agents) can request returns when allowed; admins approve or deny.

## Customer flow (request a return)
1) My Account → Orders → open the order.
2) Select the item/seat and request a return (if enabled by the store and within policy).
3) Track status on the order details page.

## Admin flow (approve/deny)
1) Sales → Orders → open order (or use the return requests list).
2) Review the return request and decide: Approve or Deny.
3) On approval: the system processes a refund and returns the seat to Available.
4) On denial: the invoice item status should revert to the previous state (no change to seat assignment).

## UI labels and behavior
- Button text may use “Refund” instead of “Unassign” when a return is initiated.
- The training link should not display for a learner without an assigned enrollment.
- Avoid manually setting order status; the integration updates statuses during returns/refunds.

## Troubleshooting
- Pending status not updating: verify the approval action completed; re-open the order to refresh.
- Failed refund shows wrong status: re-open the order; check logs and retry the refund if supported.
- Returned seat not available to reassign: confirm the return completed and the enrollment was removed.

## Related
* [Assigning and Transferring NexPort Campus Seats](assigning-and-transferring-seats/README.md)
* [Orders & Fulfillment](orders.md)
* [Purchasing Groups](purchasing-groups.md)
