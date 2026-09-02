# Migration and Durable Format Safety

Read for schemas, stored-data migrations, package/import/export formats, irreversible transformations, compatibility readers, or rollback/recovery paths.

- Assume old real user data must continue to open. Prefer additive evolution, compatibility shims/readers, copy-forward migration, backups, or explicit migration paths over abrupt breaks.
- Do not perform irreversible in-place transformation without approval. Do not silently change the contents of portable exports/backups/packages.
- Before a material format/schema change, establish affected data, backward/forward compatibility, migration behavior, failure/partial-data handling, and rollback/recovery. State what portable data now includes/excludes when that changes.
- New format versions should read older exported files/packages by default unless an intentional break is approved.
- Verify representative old/new/malformed data and interrupted/recovery paths when practical. Do not call a migration safe without evidence appropriate to its risk.
