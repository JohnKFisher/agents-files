# Tauri / Desktop WebView

Read for Tauri/Rust + WebView architecture, IPC, desktop frontend frameworks, WebView2/WebKit differences, Tauri permissions/security, or packaging.

- Treat the web frontend as the UI layer, not an unrestricted web app. Keep dependencies light; do not introduce React/Vue/heavy frameworks without clear justification and approval.
- Respect Tauri boundaries: system/filesystem/shell access goes through narrow validated IPC/capabilities. Do not bypass allowlists or expose broad unsafe commands.
- Keep frontend, Rust backend, IPC, filesystem/shell, and permission responsibilities explicit.
- When supporting macOS and Windows, account for WebKit/WebView2 and platform rendering/behavior differences rather than assuming identical behavior.
