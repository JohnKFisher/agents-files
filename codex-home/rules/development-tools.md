# Development / Review Tooling

Read when Graphify, generated architecture/context output, `/grill-me`, or similar explicit review tooling is relevant.

- Generated architecture/context such as `graphify-out/` is optional orientation, not default startup context. Do not read, regenerate, or update it for ordinary localized work. Use/update it only when the user asks, architecture/dependency relationships materially matter, or project structure changed enough that existing generated context would mislead.
- `/grill-me` is explicit critique/review mode. Do not invoke, simulate, or optimize for it unless the user asks.
- Generated tool output does not outrank current source, tests, or explicit project decisions.

## Known Codex/macOS environment recoveries

Use only when the matching failure occurs; do not perform these proactively.

- If `apply_patch` fails before reading a file with a writable-root/symlink-component error, treat it as a host sandbox issue rather than retrying path variations; use a narrowly scoped approved fallback and remove `.orig`/`.rej` artifacts afterward.
- If Swift signing/build fails because of Finder metadata/resource-fork errors, retry in a fresh build directory under `/private/tmp` rather than modifying source files.

## Codex script execution

Run repository `./scripts/*` commands with `sandbox_permissions=require_escalated` on the first attempt.

The default Codex sandbox is known to cause SwiftPM/SwiftUI macro plugin startup failures involving `sandbox-exec` or plugin-server errors. Do not spend an initial run rediscovering this known failure.