# agents-files

Opinionated `AGENTS.md` and agent-rule files for MY local-first software projects.

These are the real agent files I use across my own projects. They are published as a shareable source repo so other people can copy the parts they want and adapt them deliberately.

This is not a universal standard, not a generic framework, and not a promise that every rule belongs in every project.

## How to use this repo

Copy the files that fit your project:

- put `AGENTS.md` in the project root
- put `CLAUDE.md` in the project root if you use Claude Code
- copy only the `docs/agent-rules/*.md` files that actually fit the project
- use `docs/DECISIONS.md` and `docs/WHERE_WE_STAND.md` as starter project docs when they are useful

Treat this repo as copy-and-adapt source material, not something you need to fork wholesale.

## What you must personalize

If you adapt these files for your own work, review and change the John-specific defaults before shipping anything:

- About-screen credit rules currently point at John Kenneth Fisher
- some Apple bundle ID guidance defaults to `com.jkfisher.<appname>`
- the `local-rtk` rule is only relevant if `rtk` exists in your environment
- some rule files may not fit your stack, platform, or workflow and should be omitted

## What's here

- `AGENTS.md`: the main root instruction file
- `CLAUDE.md`: a small pointer for Claude Code sessions
- `docs/agent-rules/`: conditional rule files for specific kinds of work
- `docs/DECISIONS.md`: a minimal starter decision log template
- `docs/WHERE_WE_STAND.md`: a minimal starter status template

## Notes

These files were developed through real project use, refined over time, and improved with AI assistance alongside my own judgment.

## License

MIT
