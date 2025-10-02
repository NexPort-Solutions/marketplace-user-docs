# AGENTS: NexPort Marketplace Docs

Scope
- This file governs the entire repository. Follow these instructions for any file you add or modify.

Purpose
- This repo contains end‑user and admin documentation for NexPort Marketplace.
- Documentation is authored in Markdown and organized for GitBook.

Location (Important)
- All GitBook content lives under `user-docs/`.
- The GitBook entry files are `user-docs/README.md` and `user-docs/SUMMARY.md`.
- Images and other assets should be stored under `user-docs/assets/`.

Authoring Rules (GitBook‑Friendly)
- Markdown only. Avoid raw HTML and complex embeds.
- Use relative links between pages (e.g., `../admin/products.md`).
- Keep headings concise and semantic.
- Heading hierarchy: one H1 (`#`) per page for the title. Use H2 (`##`) for top‑level sections, H3 (`###`) for subsections, and H4 (`####`) only when truly necessary.
- Do not skip heading levels (e.g., don’t jump from H2 to H4). Avoid using bold text as a “fake” heading.
- Align the page H1 with the intent of the item in `SUMMARY.md` (the SUMMARY label can be longer; the H1 should stay concise).
- Bullets should be short, one line where possible.
- Use blockquotes for callouts: `> Note`, `> Tip`, `> Warning`.
- Keep pages focused; split very long topics when a natural break exists.
- No secrets, tokens, or internal bug‑tracker links in public docs.
 - Place End User pages under `end-user-guide/` and Admin pages under `admin-guide/`. GitBook may create these group folders automatically via UI; keep the repo aligned with that structure.
 - Internal links: always use Markdown link syntax with relative paths (e.g., `[Orders & Fulfillment](orders.md)` or `[Assigning and Transferring NexPort Campus Seats](assigning-and-transferring-seats/README.md)` when linking to a grouped page).

Interleaving nopCommerce Docs (Single‑System Voice)
- Treat NexPort Marketplace as a unified system built on nopCommerce. Write flows as “how to do X in NexPort Marketplace,” with callouts for “NexPort enhancements” where behavior differs from stock nopCommerce.
- Do not copy or link to nopCommerce docs in published content. Instead, incorporate the necessary guidance directly into these pages in hosted context.
- Use a short “Related” section at the bottom of pages to link to other internal topics only.
- When a nopCommerce feature is required by a NexPort feature (e.g., categories before products), mention that dependency inline and describe the relevant steps succinctly.

Out‑of‑Scope (Hosted‑Only Policy)
- We are a fully hosted solution. Exclude or avoid linking to:
  - Installation and upgrading guides (local, Windows/Linux, Azure, pre‑installed)
  - Hosting provider lists, private cloud, premium services, “hire a partner” marketing pages
  - Server configuration content not applicable to hosted tenants
- Do not link to external nopCommerce docs. Cover applicable admin‑area usage topics (catalog, orders, customers, discounts, ACL, security) within our docs.

Linking Policy
- Internal links only between our pages (relative paths). No external links to nopCommerce docs in published content.
- Do not link to installation, upgrade, hosting, private cloud, or premium services.

Project Structure
- `user-docs/` — GitBook docs root
  - `README.md` — Overview/landing page
  - `SUMMARY.md` — GitBook table of contents (required)
  - `end-user-guide/` — End‑user guides (group)
    - `README.md` — Group landing page (required for the heading)
    - `*.md` — End‑user topics
  - `admin-guide/` — Admin guides (group)
    - `README.md` — Group landing page (required for the heading)
    - `*.md` — Admin topics
  - `reference/` — Glossary and reference
  - `nopCommerce-Docs-master/` — Local copy of nopCommerce docs (editor reference only; do not publish or link)
- `assets/` — Images and static assets (create as needed)
- Repo root — Reference source materials only (e.g., whitepaper PDF, workflow docs, test suite). Do not reference internal links/IDs in published docs.

Style & Terminology
- Product names: NexPort Marketplace, NexPort Campus, nopCommerce.
- Prefer conceptual phrasing like “Organization purchases”, “seats”, and “Assigning and Transferring NexPort Campus Seats” in page titles. Reserve “wholesale” for explicit UI/setting labels (e.g., sale model = wholesale).
- Use Title Case for section headers; sentence case for body text.
- Prefer active voice and present tense.
- Keep link text meaningful (avoid “click here”).
- When listing UI, match observed labels (e.g., `Administrator`, `Create/Edit Mapping`, `Redeem`).

Navigation Updates
- Any new page must be added to `user-docs/SUMMARY.md` to appear in GitBook navigation.
- Group headings must point to a folder `README.md` (e.g., `end-user-guide/README.md`, `admin-guide/README.md`). GitBook uses that `README.md` as the main page for the heading.
- Use lower‑case filenames with hyphens: `my-new-page.md`.
- Where relevant, include a short "See also (nopCommerce)" list at the bottom of the page.

Admin Guide Organization
- Under Admin Guide, structure topics into two sections aligned with nopCommerce:
  - Getting Started: initial configuration and setup (e.g., Admin Overview, Stores & Branding, Extensions & Payments, Registration Fields, Supplemental Info & Groups).
  - Running Your Store: catalog, mapping, orders, organization purchases, and seats (e.g., Products, NexPort Mapping, Assigning/Transferring Seats, Email Redemption Links, Purchasing Groups, Orders, Reporting).
- When adding a new admin topic, choose the appropriate section and update `user-docs/SUMMARY.md` accordingly.

Headings with Subpages
- It’s valid (and common) for GitBook to turn a page into a folder with a `README.md` and subpages (e.g., `admin-guide/assigning-and-transferring-seats/README.md`).
- When this happens, update any internal links to point to the folder path or its `README.md` explicitly (e.g., `assigning-and-transferring-seats/README.md`).
- Subpages live under the same folder. Add them to `SUMMARY.md` beneath the parent heading if you want them surfaced in the sidebar.
 - SUMMARY example:
   - `[Assigning and Transferring NexPort Campus Seats](admin-guide/assigning-and-transferring-seats/README.md)`
   - `  * [Sub Page Test](admin-guide/assigning-and-transferring-seats/sub-page-test.md)`

Content Sources (internal)
- Whitepaper (`Nexport Market Whitepaper.pdf`)
- Workflow notes (`SH Workflows in Marketplace.docx`, `SHCOE Workflows in Marketplace.docx`)
- Test suite (`nexport_campus_tests.xlsx`)
- When importing details, rewrite for customer‑facing clarity; exclude internal case IDs/links.

Operational Notes
- Do not document or recommend manually setting nopCommerce order status to Complete for mapped products (breaks redemption).
- Call out store‑level differences when features vary by brand/environment.
- Use examples with placeholder or example domains; avoid exposing real customer data.

Versioning & Link Maintenance
- Pin guidance to a supported nopCommerce major.minor baseline (e.g., 4.60/4.70) when possible; update links if the docs structure changes.
- Perform a quarterly link check for external references; repair or replace as needed.

Contribution Workflow
- One topic per PR; keep diffs small and focused.
- Validate Markdown renders correctly in GitBook (headings, lists, links, images).
- If adding images, compress and keep widths reasonable (≤1200px preferred) and store under `user-docs/assets/`.
- Update `user-docs/SUMMARY.md` alongside any new page.

Known Page Map (baseline under `user-docs/`)
- Overview: `README.md`
- End User: `end-user-guide/` (getting started, registration, purchasing, redeeming, scholarships, FAQ)
- Admin: `admin-guide/` (overview, stores, products, mapping, fixed vs open‑ended, scholarships/seats, wholesale, supplemental info, registration fields, orders, extensions/payments, reporting)
- Reference: `reference/glossary.md`, `nopcommerce/index.md`

Contact
- If requirements change (new flows, labels), update both the relevant page(s) and this AGENTS file when guidance needs to change.

GitBook Variables
- Use variables defined in `user-docs/.gitbook/vars.yaml` via inline expressions: `<code class="expression">space.vars.PRODUCT_NAME</code>`.
- Prefer variables for frequently repeated names (e.g., product name) rather than hard‑coding strings across pages.
- If you add a new variable in GitBook, reference it as `space.vars.YOUR_KEY` in Markdown. Coordinate default values with the docs team.
- Do not commit secrets into variables; GitBook variables are for display content only.
- Example usage appears in `user-docs/README.md` and several pages.

Mermaid Diagrams
- Use fenced code blocks with the `mermaid` language fence:
  ```
  ```mermaid
  flowchart LR
    A[Available]
    B["Awaiting (emailed)"]
    C[Assigned / Redeemed]
    A -- Assign --> C
    A -- Email redemption --> B
  ```
  ```
- Quote node labels that include parentheses, slashes, or special punctuation to ensure GitBook’s Mermaid renderer parses them (e.g., `B["Awaiting (emailed)"]`).
- Keep separate diagrams where admin and store (purchasing agent) flows differ; label sections clearly (e.g., "Status flow (Admin)" and "Status flow (Store)").
- Validate diagrams in GitBook after sync; if rendering fails, check for quoting on node labels and consistent code fences.
