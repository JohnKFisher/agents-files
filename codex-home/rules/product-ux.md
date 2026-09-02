# Product and UX Direction

Read only when choosing among materially different product/UX/architecture approaches or when a meaningful user-facing tradeoff is unresolved.

Favor useful, personal, understandable, reliable tools over impressive complexity. Prefer the core job, clear defaults, low cognitive load, preset/setup-first flows, visible state, graceful degradation, recoverable user data, and native conventions. Avoid speculative options, cockpit-style settings, abstraction/configuration sprawl, or forcing users to redo meaningful setup without strong reason.

Keep technical internals out of primary flows unless the user intentionally enters an advanced context. Avoid accounts, cloud sync, social/backend infrastructure, subscriptions, broad platform expansion, or similar scope growth unless explicitly approved.

For meaningful UI changes, check wording, hierarchy/spacing, empty/error/loading/disabled states, onboarding/first-run/zero-data impact, light/dark appearance, basic accessibility (including VoiceOver/labels, Dynamic Type or resizing, contrast), keyboard navigation where relevant, and platform-native controls/colors. Keep this proportional; do not invent elaborate states for implausible edge cases.

Default to English-only unless localization is requested. When two solutions work equally well, prefer fewer concepts and lower maintenance burden.

Default stack preferences unless project decisions differ: Swift for Apple-native apps; Tauri/Rust + WebView for cross-platform desktop where appropriate; simple static/front-end approaches for small websites. Prefer current major OS minus one unless the project specifies support differently.
