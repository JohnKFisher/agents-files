# Dependencies, Assets, Licensing, and Credits

Read for third-party packages/binaries, package manifests/lockfiles, bundled media/fonts/assets, licensing/attribution, About/credits surfaces, or redistribution claims.

- Prefer native/platform/project APIs and small local implementations when reasonable. Add third-party dependencies only when justified by meaningful risk/complexity/maintenance benefit; avoid convenience-only packages, broad upgrades, package-manager churn, and unrelated lockfile rewrites.
- Before adding a redistributed dependency/tool/asset, establish source/provenance, license, commercial/App Store/distribution safety, attribution requirements, and source-disclosure obligations. Prefer options whose licensing is compatible with the project's intended use and distribution.
- Never scrape random media/assets for bundling. Do not redistribute fonts unless clearly licensed and explicitly appropriate. Track required attribution (for example in `ATTRIBUTIONS.md`) and surface it in About/Licenses where required.
- Existing project licenses are durable; never change them without explicit instruction. Do not choose a license for a new project without considering its intended use and distribution requirements.
- About/credits surfaces default to copyright credit `Sidelark Labs ; John Kenneth Fisher`, plus clickable Sidelark Labs/public GitHub links when the surface supports links and they exist and required third-party acknowledgments.
- Do not overstate packaged-build portability, signing/notarization, architectures, OS support, bundled dependencies, or external requirements.
