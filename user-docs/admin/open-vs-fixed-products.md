# Fixed vs Open‑Ended Products

Fixed products
- Represent a specific training item (course, bundle, section) and map directly to one NexPort item.

Open‑ended products
- Let an admin or student select from a defined list of fixed products at assignment time.
- Useful when the purchase is for “one of these courses” rather than a specific one.

Create fixed products
1) Create the product in `Catalog` → `Products` and set price/publish.
2) Map it to the target NexPort item under `NexPort Product Mappings`.

Use open‑ended products
1) Create a NopCommerce product that represents the choice.
2) Configure its mapping to reference the allowed list of fixed products (as supported by your plugin/build).
3) When assigning, select which fixed product the learner receives.

Notes
- Open‑ended assignments select from fixed products at redemption/assignment time.
- Ensure all fixed options are published and mapped.

