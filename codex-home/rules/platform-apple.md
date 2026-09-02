# Apple Platform

Read when Apple-specific capabilities, entitlements, signing/notarization, sandbox/App Store/TestFlight, privacy prompts, PhotoKit/MusicKit, lifecycle/state ownership, startup/main-thread performance, media/import/export, or compatibility can materially affect the plan. Skip for ordinary localized Swift/UI edits.

- Prefer documented current Apple APIs and native lifecycle/UI/accessibility patterns. Avoid private APIs, undocumented system behavior, and private on-disk paths as stable inputs. Use deprecated APIs only when compatibility requires them and note the migration path.
- Bundle IDs are durable identity; default new personal IDs to `com.sidelarklabs.<appname>`. Do not change bundle IDs, targets/extensions, capabilities, entitlements, signing, privacy strings, App Store metadata, or release behavior without explicit task/approval.
- For capability-dependent code, verify project settings/entitlements/provisioning assumptions and graceful denied/restricted/unavailable states. Flag review-sensitive changes involving protected data/services, background modes, IAP/subscriptions, analytics/tracking, collection/retention/export/upload/sharing.
- Keep processing local unless network behavior is explicitly requested/established.
- Protect launch and UI responsiveness: no expensive indexing/media/network/file scans/migrations/package parsing in startup or SwiftUI body without justification; keep expensive non-UI work off the main actor, bound memory/caches/tasks/observers, and use async progress/cancellation where appropriate.
- Prefer native system colors/type/controls and straightforward state flow; avoid unnecessary UI frameworks/style systems/abstraction.
