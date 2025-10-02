# Admin Overview

This overview explains how the storefront (nopCommerce) and training platform (NexPort Campus) work together in <code class="expression">space.vars.PRODUCT_NAME</code>, and what admins manage day to day.

## Platform components
- nopCommerce (storefront): Stores, products, pricing, checkout, payments, orders.
- NexPort Campus (training): Sections (courses), Training Plans (curricula), Catalogs, enrollments, reporting.
- Integration: Product mappings connect store products to NexPort items; purchases create seats that become enrollments when redeemed.

## Core concepts
- Section (NexPort): A single course. Purchasing and redeeming creates an enrollment in that course.
- Training Plan (NexPort): A structured set of courses (curriculum). Redeeming enrolls the learner in the plan’s items per the plan rules.
- Catalog (NexPort): A curated collection of courses; used for open‑ended selections and program access.
- Product (nopCommerce): A sellable item in a store; can be mapped to a Section, Training Plan, or Catalog.
- Store (nopCommerce): A branded storefront with its own catalog, pricing, and policies.
- Mapping: Links a product to a NexPort item. One NexPort item can be reused and mapped to multiple products across multiple stores. Default mapping + per‑store overrides control behavior.
- Seat (redemption): A purchased entitlement created by a product mapping. Seats can be auto‑redeemed or manually redeemed/assigned later.

## Mapping and reuse across stores
- Create a default mapping for the product to a Section, Training Plan, or Catalog. Then add per‑store mappings as needed.
- Reuse: The same NexPort item can be mapped to different products in different stores to tailor branding, pricing, and policies without duplicating training content.
- Overrides: Per‑store mapping can set redemption mode (auto or manual), subscription organization, and other options.

## Purchase‑to‑seat lifecycle
1) Customer buys a product. If quantity > 1, multiple seats are created.
2) If auto‑redeem is enabled, the system creates the enrollment(s) after payment completes.
3) If manual, the purchaser (store side) or an admin assigns seats later. Seats can also be distributed via email redemption links.
4) On redemption, seats become enrollments in NexPort; the learner sees training links and begins coursework.
5) Seats can be unassigned/transferred when appropriate, or returned/refunded per policy.

## Assignment options
- Admin assign: Sales → Orders → open order → assign seats to learners. Supports transfer/unassign.
- Store‑side assign: Purchaser uses My Account → Orders to assign or email redemption links.
- Email redemption: Send a link; status moves to Awaiting until the recipient redeems or the sender cancels.

## Typical workflows
- Retail purchase: Single learner buys and is auto‑enrolled (or redeems manually) in a course/plan.
- Organization purchase: Purchasing agent buys multiple seats across courses; assigns seats to learners directly or via email; can transfer/return seats later.
- Open‑ended selection: Product mapped to a Catalog lets the assignee pick a specific course at redemption.

## Access the admin area
1) Sign in to your store with an admin account.
2) Click the `Administrator` banner at the top to open the Admin Dashboard.

## Related
* [Stores & Branding](stores.md)
* [Products](products.md)
* [NexPort Mapping](nexport-mapping.md)
* [Assigning and Transferring NexPort Campus Seats](assigning-and-transferring-seats/README.md)
* [Email Redemption Links for Seats](email-redemption-links-for-seats.md)
* [Orders & Fulfillment](orders.md)
