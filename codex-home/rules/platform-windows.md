# Windows Platform

Read for Windows builds/CI, PowerShell, paths, WinUI/Fluent conventions, installers/packaging, resources, signing, or SmartScreen.

- Prefer native Windows conventions and Fluent/WinUI for native apps; cross-platform apps may differ visually by platform.
- Windows builds are unsigned unless the user establishes signing. Prefer portable/per-user distribution over admin/system-wide MSI unless the project requires otherwise.
- Handle path-length limits, reserved names (`CON`, `PRN`, `NUL`, etc.), separator differences, and Windows filesystem semantics intentionally; do not assume Unix behavior.
- Windows CI must not assume Unix shells/commands; use PowerShell or verified cross-shell behavior.
