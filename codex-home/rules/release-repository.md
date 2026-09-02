# Repository, CI, Release, Packaging, and Distribution

Read for commits/branches/worktrees/tags/history recovery, version source files, CI, signing/notarization, packaging/installers, App Store/TestFlight, or public release/distribution workflows.

## Repository safety

Do not commit, push, tag, merge, rebase, reset, cherry-pick, switch/create/delete branches, or create/delete worktrees unless explicitly requested. The user manages branch/worktree strategy. Before destructive recovery/history operations, inspect current state, identify unrelated/uncommitted work and the restore target, explain likely loss, and prefer reversible recovery. Never discard user work implicitly.

When asked to commit, inspect the diff, keep it focused, and exclude secrets, user data, logs, caches, and unrelated generated artifacts. When useful after meaningful successful work, you may suggest (not create) a known-good commit/tag/status checkpoint. Force-push/history rewrite/remote branch deletion requires explicit direction with risk understood.

## Release safety

Treat the existing workflow/scripts/config as ground truth. Ask before materially changing release topology, signing/notarization, installer behavior, deployment triggers, permissions, public distribution behavior, bundle IDs, marketing versions, entitlements/privacy strings, or release metadata. Modify known-good workflows surgically rather than inventing replacements.

Never hardcode secrets, certificates/profiles, personal paths, or machine-specific values. Use least-privilege CI permissions, limited artifact retention, and current supported actions/runtimes. Do not mutate tracked source in CI unless intentionally designed.

When creating a new desktop packaging flow after approval, reasonable defaults are macOS `.app` in `.dmg` and Windows portable `.exe` unless installer requirements say otherwise; artifact names should identify app, platform, and packaging style.

Version-triggered releases derive tags/names from the checked-in version source; never move published tags silently. Prefer a new patch/build for post-release fixes, and base release notes on actual changes rather than placeholders.

## App version/build convention

For application repositories, the preferred convention is checked-in root files:

- `VERSION` — authoritative marketing/app version
- `BUILD_NUMBER` — authoritative build number

If both files exist, treat them as the single source of truth. Do not independently maintain conflicting version/build values elsewhere.

Before **every actual app build**, including builds run for development, testing, validation, archive, or release:

1. read the current checked-in `BUILD_NUMBER`;
2. increment it exactly once;
3. write the new value back to `BUILD_NUMBER` before invoking the build;
4. leave `VERSION` unchanged unless the user explicitly requests a version change;
5. ensure the build consumes the checked-in values;
6. report `BUILD_NUMBER` as `old -> new`.

Each separate build invocation receives its own increment. Never reuse a build number merely because a prior build was local, failed, or was not distributed.

For a new app, establish this convention during initial build/version setup.

For an existing app that does not yet use this convention:
- when the task creates, replaces, or materially changes version/build plumbing, retrofit to this convention by default unless a concrete project constraint makes it unsuitable;
- for unrelated work, do not expand scope solely to retrofit versioning, but mention the missing convention when it is directly relevant.

A retrofit must first determine the app's current effective version and build number. Preserve those as the initial `VERSION` and `BUILD_NUMBER`; do not reset or invent values. Then make the root files authoritative, update build/project configuration to consume them, eliminate independently maintained conflicting values where safely possible, preserve existing release behavior, and verify the built artifact receives the expected values.

If the platform or build system prevents a true single source of truth, preserve the root files as authoritative inputs and document the minimum necessary derived/generated values.

Marketing/app version changes always require explicit user direction. Build-number increments required by this convention do not.

## Distribution honesty

Never imply commit/push/tag/upload/sign/notarize/release/remote-run success unless it occurred. State unsigned/ad-hoc/unnotarized/host-specific or Gatekeeper/SmartScreen limitations clearly.

Verify changed workflow syntax/triggers/permissions/artifact paths and relevant local packaging behavior where practical. For CI failures, inspect the failing job/step before rerunning or rewriting workflows.
