# NexPort Mapping

Mapping connects a NopCommerce product to a NexPort product/section and defines store‑specific behavior.

Where to find mapping
- Edit a product and scroll to `NexPort Product Mappings`.
- Use `View Nexport Product` to switch to the mapping section, or `Synchronize from Nexport` after section updates.
- Use the mapping search/filter above the list.

Create the default mapping
1) Edit the product.
2) Click `Create/Edit Mapping` (Default Mapping). Other mapping actions are disabled until a default exists.
3) In the mapping window, select the target Nexport product/section.
4) Choose `Auto‑redeem` or keep manual redemption.
5) Save.

Store mappings
- After a default mapping exists, create per‑store mappings to override defaults (e.g., price, subscription org, redemption mode).

Subscription organization selection
1) In the mapping window, start typing the organization name.
2) Pick from predictive results. The org GUID and names populate automatically.
3) Save.

Editing, deleting, and copying mappings
- Modify any mapping to update behavior.
- Remove store mappings if no longer needed (default mapping remains).
- Copying a product can also copy mappings when specified.

Best practices
- Prefer auto‑redeem for frictionless learner experiences unless supplemental intake is required.
- Do not change NopCommerce order status manually; let the plugin update the order when redemption occurs.

