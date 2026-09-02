# Media, Rendering, Export, and Output Quality

Read for media import/export, encoding/rendering, generated files, filenames/temp cleanup, color/HDR/brightness, timing, audio/video, thumbnails/metadata/codecs, or final artifacts.

The final artifact is protected product behavior. Do not trade away fidelity, determinism, compatibility, or user trust merely for speed or implementation convenience.

- Before a materially heavier, lower-quality, less-compatible, or output-changing approach, establish baseline behavior, expected impact/risk, safer/no-regression alternatives, and a recommendation. If baseline evidence is missing, measure before claiming improvement.
- Consider codec/playback compatibility, cadence/timing, A/V sync, dimensions, metadata, expected viewers, color/HDR behavior, and output size where relevant. Successful export alone does not prove acceptable quality.
- Keep codec/encoder/render internals out of primary consumer flows unless intentionally advanced.
- Resolve user-visible filenames/output paths clearly; prefer shared source-of-truth helpers over duplicated patches. Treat filenames/metadata as untrusted input when they cross tool/shell boundaries.
- Temp cleanup is restricted to app-owned temp roots. Never clean source media/libraries or final exports implicitly.
- Verify output-affecting changes with targeted behavioral/media checks plus builds/smoke tests proportional to risk. For fidelity/performance claims, use actual before/after evidence when practical.
