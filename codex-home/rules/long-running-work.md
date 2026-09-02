# Long-Running, Background, Queue, and Sync Work

Read for expensive/background operations, queues, uploads/downloads, sync/scheduling, large scans/indexing, progress, cancellation/resume/retry, subprocess orchestration, partial output, or temp cleanup.

- Provide clear liveness/progress; avoid blocking UI. Prefer cancellable, resumable, or recoverable work where practical.
- Bound concurrency and memory. Prefer event-driven updates to polling; stream/page/batch large data where feasible.
- Preflight cheap blockers before expensive work: inputs, output paths, capabilities/tools, permissions, and storage when relevant.
- Errors must be explicit/actionable. Do not hide retries, fallback backends, uploads/writes/overwrites, permission expansions, or quality changes that materially affect output, privacy, cost, or reliability.
- Prefer atomic finalization (temp + verified rename/move). Clean only app-owned temporary artifacts on success/failure/cancel unless retention is deliberately needed for recovery/debugging.
- Prefer graceful cancel/shutdown; force-kill only as a last resort. Use bounded waits/timeouts/liveness checks; do not hang indefinitely. Distinguish unavailable, stale, empty, unauthorized/denied, failed, and not-yet-configured states.
- For multi-source/sync designs, normalize source-specific data before core/UI logic, keep connector quirks at the edges, prevent duplicate scheduled execution, and record enough execution state to know whether/how work ran.
- Do not overwrite existing generated outputs unless that behavior is explicit and safe.
