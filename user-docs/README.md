# NexPort Marketplace Documentation

NexPort Marketplace is a multi‑store e‑commerce layer for distributing learning products in the NexPort Learning Platform. It integrates with NopCommerce for storefront, payments, and extensibility, and with NexPort Campus for identity, enrollments, subscriptions, and training delivery.

This documentation covers:
- End‑user guidance for browsing, purchasing, and redeeming training
- Admin guidance for configuring stores, products, mappings to NexPort, and workflows (scholarships, wholesale, libraries)

Key capabilities
- Multi‑brand stores with independent themes, catalogs, and pricing
- Centralized courseware distribution, mapped to NexPort products/sections
- Flexible product types: courses, digital downloads, and physical goods
- Store‑level sale models (retail/wholesale) and purchasing controls
- Custom registration fields, validation, and store scoping
- Supplemental info questions that can drive group membership
- Manual or auto‑redeem flows, with safe order handling

If you’re new, start with End User → Getting Started, then see Admin → Products & Mapping if you manage catalogs.


## Terminology
- Store: A branded storefront (NopCommerce) within NexPort Marketplace.
- Product (NopCommerce): An item listed in a store (can map to a NexPort product/section).
- Fixed product: A specific course or bundle; used as concrete selections.
- Open‑ended product: A selector product that lets an assignee pick from a list of fixed products at assignment time.
- Mapping: The association between a NopCommerce product and a NexPort product/section, with store and subscription context.
- Auto‑redeem: Purchase creates/assigns training automatically after payment is completed.
- Manual redeem: Customer must click Redeem on Order Details to create training.
- Scholarship/Seat: A pre‑purchased entitlement that can be assigned to learners (e.g., libraries or organizations).


## Environments (examples)
Your organization may maintain multiple environments for testing vs. production. Example URLs found in test materials include: `nexportmarket.com`, `alpha.nexportmarket.dev`, and industry/partner‑specific branded domains. Consult your team for the current environment list and access.

