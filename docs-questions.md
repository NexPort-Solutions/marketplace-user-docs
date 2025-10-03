# Documentation Questions Backlog

This backlog lists open questions to answer so we can improve and finalize the NexPort Marketplace docs. Answers should be reflected in the linked pages under `user-docs/`.

## Versioning & Environments
- [ ] What nopCommerce version(s) do hosted tenants run (e.g., 4.60/4.70) to anchor terms/screenshots?
- [ ] Which environment URLs can we reference as examples (dev/stage/prod) without exposing sensitive data?
- [ ] Any store-specific UI label differences we should call out in screenshots/captions?

## Products & Mapping
- [ ] Do we support mapping to NexPort Catalogs for open-ended selection in production? Any constraints to document? (user-docs/admin-guide/open-vs-fixed-products.md)
- [ ] What are the exact UI labels/locations for mapping actions: "Create/Edit Mapping (Default)", per-store overrides, "Synchronize from NexPort"? (user-docs/admin-guide/nexport-mapping.md)
- [ ] When copying products, under what conditions are mappings copied vs reset? Any warnings needed? (user-docs/admin-guide/products.md)
- [ ] Do we support "Extension only" products universally? Any store exceptions? (user-docs/admin-guide/products.md, user-docs/admin-guide/extensions-and-payments/enrollment-extensions.md)

## Seats: Assigning, Transferring, Unassigning
- [ ] Are there policy limits on how often a seat can be reassigned or time windows to restrict transfers? (user-docs/admin-guide/assigning-and-transferring-seats/README.md)
- [ ] Clarify "Delete Finished" constraint: exact conditions that block unassign vs transfer and the recommended admin steps.
- [ ] Should we document role/permission requirements for who can assign/unassign at the store vs admin level?

## Orders & Fulfillment
- [ ] Confirm gateways in use and whether authorize-then-capture is common; when does auto-redeem fire relative to capture? (user-docs/admin-guide/orders.md)
- [ ] What admin actions are allowed post-payment on mapped items (edit lines, change qty) without risking desync, or should these be strongly discouraged?
- [ ] How should partial refunds map to seat reclamation when multiple quantities exist on a single line? Add an example? (user-docs/admin-guide/orders.md, user-docs/admin-guide/returns-and-refunds-for-seats.md)
- [ ] Any tenant that sells physical goods with training in mixed carts? If so, confirm shipping guidance and examples. (user-docs/admin-guide/orders.md)

## Returns & Refunds
- [ ] What is the official returns window/policy for seats by store/brand? Do we need a policy template? (user-docs/admin-guide/returns-and-refunds-for-seats.md)
- [ ] Do partial returns ever keep some learners enrolled while reclaiming others on the same order? Include a diagram?
- [ ] Are there gateway-specific caveats for refunds (full vs partial) we should call out?

## Email Redemption Links
- [ ] Do emailed links expire? If so, after how long and is it configurable per store? (user-docs/admin-guide/email-redemption-links-for-seats.md)
- [ ] Are there throttles/limits on resending, and do we log resend reasons the admin can see?
- [ ] Can purchasers bulk-email redemption links for high quantities? Any UI/path we should document?

## Purchasing Groups & Organization Purchases
- [ ] How are Purchasing Groups created/managed today (UI path)? Should we add a step-by-step? (user-docs/admin-guide/purchasing-groups.md)
- [ ] Can seats be moved between groups after purchase? If yes, who can do it and how is reporting affected?
- [ ] Any cross-store visibility rules for agents managing seats across multiple brands?

## Registration Fields & Supplemental Info
- [ ] Where exactly are Registration Fields configured in hosted tenants (menu path)? Include screenshots? (user-docs/admin-guide/registration-fields.md)
- [ ] For Supplemental Info, can questions be reused across products/stores? Any migration steps when options change? (user-docs/admin-guide/supplemental-info.md)
- [ ] Common field validations (e.g., library card regex) we should include as examples or link to reference patterns?

## Extensions & Payments
- [ ] Which payment gateways are supported across our hosted tenants (names + capture/refund capabilities)? (user-docs/admin-guide/extensions-and-payments/payment-methods.md)
- [ ] Do we support taxes and multiple currencies for training products, and where are the hosted-safe toggles? (user-docs/admin-guide/extensions-and-payments/currencies-and-taxes.md)
- [ ] For Enrollment Extensions, what thresholds/approval rules are actually used in production? Provide concrete examples. (user-docs/admin-guide/extensions-and-payments/enrollment-extensions.md)

## Reporting & Analytics
- [ ] Which order export fields are required for finance reconciliation of seats and refunds? Provide a canonical CSV/Excel column list. (user-docs/admin-guide/reporting.md)
- [ ] Should we add a "Seat utilization" report example (queries/filters) to make assignment monitoring clearer?
- [ ] Any standard cross-report workflow between store exports and NexPort Campus completion reports we should document?

## Roles, Permissions, and ACL
- [ ] What roles/permissions are required for: viewing orders, assigning seats, approving returns, editing mappings? (Map to nop ACL names)
- [ ] Do purchasing agents have limits on which learners they can assign (e.g., within their Purchasing Group only)?
- [ ] Should we include a minimal "Access Control" reference page under Admin → Getting Started?

## End-User Guides
- [ ] Add an "Email redemption troubleshooting" page for recipients? What top issues should it cover? (user-docs/end-user-guide/redeem-training.md)
- [ ] Any environments where guests can purchase vs enforced account creation before checkout? Clarify the shopper flow. (user-docs/end-user-guide/browsing-and-purchasing.md)

## Screenshots & Assets
- [ ] Provide sanitized screenshots for: Products (mapping panel), NexPort Mapping dialog, Orders (seat actions), Assign/Unassign flows, Returns approval. (See Memento TODOs)
- [ ] Where should we store brand-generic screenshots vs store-specific variants? Create `user-docs/assets/` structure?
- [ ] Any redaction rules (emails/names/order numbers) we must follow before publishing images?

## Diagrams (Mermaid)
- [ ] Validate admin and store status-flow diagrams; any additional states or branches to include? (user-docs/admin-guide/assigning-and-transferring-seats/README.md)
- [ ] Add a compact returns decision diagram (Approve/Deny) to the returns page? (user-docs/admin-guide/returns-and-refunds-for-seats.md)

## GitBook Structure & Variables
- [ ] Should we remove the placeholder subpage `admin-guide/assigning-and-transferring-seats/sub-page-test.md` or replace with concrete examples?
- [ ] What additional GitBook variables are useful (e.g., COMPANY_NAME, SUPPORT_URL, SUPPORT_EMAIL)? Add to `user-docs/.gitbook/vars.yaml` and update pages accordingly.
- [ ] Confirm we keep orders content on a single page vs breaking out Shipping/Settings later. (user-docs/admin-guide/orders.md)
- [ ] Should `reference/README.md` be expanded into an index or removed to avoid redundancy with the Glossary?

## Policies & Compliance
- [ ] Any privacy, data retention, or accessibility statements we should link from the Overview? (user-docs/README.md)
- [ ] Do we have standard return/refund policy language per store that we can re-use in examples?

## Glossary
- [ ] Are any key terms missing (e.g., "Owner Group", "Purchasing Agent", "Open-ended Selector")? (user-docs/reference/glossary.md)
- [ ] Should we align on preferred synonyms (seats vs scholarships) and note UI exceptions where "wholesale" appears?

## Navigation & Cross-links
- [ ] Any additional cross-links you want consistently added (e.g., Products → Orders, End-user → Admin counterparts)?
- [ ] Are there store-specific topics we should branch into subpages later (e.g., industry programs)?

## Source Materials
- [ ] From `Filter.csv`, which edge cases need explicit articles vs small callouts? Provide a prioritized list.
- [ ] Any internal workflow documents (e.g., SH/SHCOE) that should be distilled into public how-to pages now?
