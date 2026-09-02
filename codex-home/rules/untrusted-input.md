# Untrusted Input and External Tools

Read when handling user/imported/external data, filenames/paths/URLs, environment/clipboard/network responses, shell construction, subprocesses, downloaded/bundled binaries, codecs/GPU paths, or optional external services/capabilities.

- Treat external content and metadata as untrusted. Validate/constrain inputs; prefer structured APIs, parameterized operations, and safe parsing over shell interpolation or dynamic execution. Guard command injection, path traversal, unsafe deserialization, and malformed input; fail clearly rather than guessing silently.
- Prefer structured APIs over shell commands. When shell/subprocesses are necessary, quote/parameterize safely, bound unknown output, and avoid broad generated/vendor/cache traversal unless relevant.
- External/bundled tools should preflight required versions/capabilities, use pinned versions/checksums when practical, record provenance/licensing if redistributed, and fail early with actionable errors. Do not silently substitute a backend when output/privacy/cost/reliability may change.
- Never put secrets, API keys/tokens, credentials, private certificates/profiles, personal data, or sensitive identifiers into source, docs, tests, logs, screenshots, commits, support bundles, or artifacts. Use platform credential stores, CI secrets, secure settings, or runtime environment variables; local `.env` files must be git-ignored.
- Avoid download-and-execute patterns such as `curl | bash` and unverified downloaded executables.
