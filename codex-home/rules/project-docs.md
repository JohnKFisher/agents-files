# Project Documentation and Release-Note Source

Read when work touches README/install/distribution docs, `docs/DECISIONS.md`, `docs/WHERE_WE_STAND.md`, `docs/WORKING_CHANGELOG.md`, or release-intended user-visible changes.

- README stays minimal, accurate, and current: briefly describe the app/tool and point to `https://sidelarklabs.com`. Do not overclaim setup, distribution, platform support, signing/notarization, compatibility, availability, or generated outputs. Do not turn README into history/planning/changelog.
- Append meaningful approved architectural/design/scope/tooling/behavioral decisions to `DECISIONS.md`; preserve superseded/reversed history.
- Update `WHERE_WE_STAND.md` only for material state/milestone/version/known-good changes or when asked. Keep it practical, not marketing copy.
- Update `WORKING_CHANGELOG.md` for release-intended user-visible changes, not tiny polish, experiments, temporary/internal-only work, or unapproved candidates. When uncertain, mention the possible entry instead of editing automatically. Write in moderately non-technical user language; avoid commit hashes/branch names/speculation. `[public candidate]` and `[needs review]` are optional lightweight markers. Do not rename an existing project changelog just to match this template.
- If code changes make existing docs materially false, update the directly affected docs or clearly report the follow-up.
- Leave concise breadcrumbs for non-obvious durable constraints; avoid comments/docs that merely narrate obvious code.
