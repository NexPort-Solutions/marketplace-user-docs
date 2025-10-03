# Enrollment Extensions

Use extension products and mappings to extend existing enrollments rather than creating new ones.

## Concepts
- Extension product: A product marked as `Extension only` that targets a mapped NexPort item which supports extension.
- Approval method: Manual vs automatic approval before an extension is processed.
- Threshold behavior: Under certain thresholds, the system may use the time limit rather than extension duration when resetting enrollments.

## Setup
1. Mark the product as `Extension only` (or allow extensions) in product settings.
2. In the mapping, enable extension behavior for the target NexPort item.
3. Choose the approval method and any thresholds required by your program.

## Operations
- Manual approval requires an admin to approve the extension before it is applied.
- Verify extension outcomes in the learner’s enrollment details.

## Related
- [NexPort Mapping](../nexport-mapping.md)
- [Orders & Fulfillment](../orders.md)
