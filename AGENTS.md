# AGENTS: NexPort Marketplace Docs

Scope
- This file governs the entire repository. Follow these instructions for any file you add or modify within this docs repo.

Purpose
- This repo contains end‑user and admin documentation for NexPort Marketplace.
- Documentation is authored in Markdown and organized for GitBook.

Authoring Rules (GitBook‑Friendly)
- Markdown only. Avoid raw HTML and complex embeds.
- Use relative links between pages (e.g., `../admin/products.md`).
- Keep headings concise; prefer H1 per page, then H2/H3 sparingly.
- Bullets should be short, one line where possible.
- Use blockquotes for callouts: `> Note`, `> Tip`, `> Warning`.
- Keep pages focused; avoid very long pages when a natural split exists.
- Images: place under `assets/` and reference with relative paths; add descriptive alt text.
- No secrets, tokens, or internal bug‑tracker links in the public docs.

Project Structure
- `README.md` — Overview/landing page
- `SUMMARY.md` — GitBook table of contents (required)
- `user/` — End‑user guides
- `admin/` — Admin guides
- `reference/` — Glossary and reference materials
- `assets/` — Images and other static assets (create as needed)

Style & Terminology
- Product names: NexPort Marketplace, NexPort Campus, NopCommerce.
- Use Title Case for section headers; sentence case for body text.
- Prefer active voice and present tense.
- Keep link text meaningful (avoid “click here”).
- When listing UI, match observed labels (e.g., `Administrator`, `Create/Edit Mapping`, `Redeem`).

Navigation Updates
- Any new page must be added to `SUMMARY.md` to appear in GitBook navigation.
- Use lower‑case filenames with hyphens: `my-new-page.md`.

Content Sources (internal)
- Whitepaper (`Nexport Market Whitepaper.pdf`)
- Workflow notes (`SH Workflows in Marketplace.docx`, `SHCOE Workflows in Marketplace.docx`)
- Test suite (`nexport_campus_tests.xlsx`)
- When importing details, rewrite for customer‑facing clarity; exclude internal case IDs/links.

Operational Notes
- Do not document or recommend manually setting NopCommerce order status to Complete for mapped products (breaks redemption).
- Call out store‑level differences when features vary by brand/environment.
- Use examples with placeholder or example domains; avoid exposing real customer data.

Contribution Workflow
- One topic per PR; keep diffs small and focused.
- Validate Markdown renders correctly in GitBook (headings, lists, links, images).
- If adding images, compress and keep widths reasonable (≤1200px preferred).
- Update `SUMMARY.md` alongside any new page.

Known Page Map (baseline)
- Overview: `README.md`
- End User: `user/` (getting started, registration, purchasing, redeeming, scholarships, FAQ)
- Admin: `admin/` (overview, stores, products, mapping, fixed vs open‑ended, scholarships/seats, wholesale, supplemental info, registration fields, orders, extensions/payments, reporting)
- Reference: `reference/glossary.md`

Contact
- If requirements change (new flows, labels), update both the relevant page(s) and this AGENTS file when guidance needs to change.

