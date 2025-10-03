# Glossary

- Auto‑redeem: Order completion automatically creates/assigns training in NexPort.
- Catalog (NexPort): A curated collection of courses used for discovery and open‑ended selections.
- Email redemption link: An emailed link a recipient uses to redeem a seat; places the seat in Awaiting until redeemed or canceled.
- Enrollment: A learner’s registration in a NexPort Section or Training Plan created by redeeming a seat.
- Fixed product: A specific mapped course/bundle.
- Mapping: Association from a nopCommerce product to a NexPort product/section, with store overrides.
- Manual redeem: Redemption requires the purchaser to click Redeem (or an admin to Assign) after payment.
- NexPort Marketplace: Hosted solution combining nopCommerce (storefront) with NexPort Campus (training) via product mappings.
- NexPort Campus: Learning platform for identity, enrollments, and training delivery.
- Open‑ended product: A product that lets an assignee pick from a set of fixed products at assignment.
- Open‑ended selector: Another term for an open‑ended product that offers a choice among fixed products.
- Scholarship/Seat: Pre‑purchased entitlement to be assigned to a learner.
- Section (NexPort): An individual course.
- Subscription Organization: The organization context selected on a mapping; enrollments and ownership follow this org unless overridden.
- Store: A branded storefront within <code class="expression">space.vars.PRODUCT_NAME</code> (nopCommerce).
- Supplemental Info: Questions asked at purchase/redemption; can drive group membership.
- Training Plan (NexPort): A curriculum comprising multiple courses; redemption enrolls the learner per plan rules.
- Wholesale: Purchasing model for buying multiple seats via authorized agents.

## Additional terms
- Purchasing Agent: A user who buys seats for others and manages assignments.
- Purchasing Group: The organization unit that owns seats.
- Owner Group: The purchasing group recorded on a seat/redemption for tracking and permissions.
- Invoice Item: A single purchased seat (or similar unit) in an order.
- Redemption: The act of creating an enrollment for a seat; may be Auto or Manual.
- Awaiting (status): An emailed redemption link has been sent but not redeemed yet.
- Return Request: A customer or admin action to return a seat and process a refund.
- Transfer: Unassigning a seat from one learner and assigning to another.
- Assign: Action that attaches an Available seat to a learner and creates an enrollment.
- Unassign: Action that detaches a seat from a learner (returns to Available) or moves it into a return flow per policy.
- Extension product: A product and mapping that extends an existing enrollment instead of creating a new one.
- Default Mapping: The base product‑to‑NexPort association required before adding per‑store overrides.
- Per‑store Mapping: A store‑specific override of the Default Mapping (e.g., price, redemption mode, subscription org).
- Delete Finished: An admin operation restricted when a learner has an active (In Progress) enrollment; resolve the active enrollment first.
- Shipping not required: Shipping status for digital/mapped training items; used on mixed orders with physical goods.

## Seat statuses
- Available: Seat exists and is not assigned.
- Awaiting (emailed): Email redemption sent; not yet redeemed by the recipient.
- Assigned/Redeemed: Enrollment created in NexPort Campus (via Assign or Redeem).
- Returned: Seat reclaimed through a return/refund flow; available for reassignment once processed.

## Order and payment statuses (overview)
- Order status: Pending, Processing, Complete, Cancelled. For mapped items, avoid forcing Complete manually.
- Payment status: Pending, Authorized (eligible to Capture or Void), Paid (eligible to Refund/Partial refund), Partially refunded, Refunded, Voided.
