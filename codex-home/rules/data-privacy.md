# Data, Files, Permissions, and Diagnostics

Read when work touches user content, local/cloud files, photos/contacts/calendars/mail/messages, bulk/destructive operations, permissions/entitlements/privacy prompts, diagnostics/logging/support bundles, or app-owned vs user-owned storage.

- Default user-content access to read-only unless writes are requested/approved. Never add deletion/destructive behavior implicitly.
- For broad or destructive writes, prefer preview/dry-run, explicit scope/counts, confirmation, and reversible alternatives where feasible. Resolve exact target paths and guard traversal, ambiguous relative paths, broad globs, and accidental all-library/all-folder actions.
- Never overwrite user-owned files or touch source media/final exports without explicit behavior/approval. Keep app/account/device state separate from portable user content unless intentionally designed otherwise.
- Exports/backups/packages must not silently include credentials/tokens, entitlement/purchase state, diagnostics, private paths, caches, or other device-local state. State what travels and what remains local when that boundary changes.
- New/changed permissions, entitlements, sandbox/capabilities, privacy strings, signing-sensitive capabilities, telemetry, analytics, tracking, ads, remote diagnostics, or background network behavior require explicit approval unless already required by the user's task/project decision. Use least privilege and graceful denied/restricted/limited states; preserve a useful read-only/local/manual degraded path when feasible rather than making denied permission unnecessarily fatal.
- Persistent diagnostics should be local, minimal, redacted, and opt-in unless approved otherwise. Do not expose or commit user data, sensitive paths/identifiers, logs, crashes, screenshots, support bundles, or sample personal data.
- User-initiated support exports should be redacted by default and previewable when feasible. Clearly distinguish local diagnostics from anything transmitted externally. Nothing phones home silently.
