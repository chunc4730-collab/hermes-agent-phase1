# hermes-agent Phase 1 Patches

5 reliability modules for [Hermes Agent](https://github.com/nousresearch/hermes-agent), delivered as clean git patches.

## What this is

A set of core-level en...[truncated]
## Why

These patches make Hermes more reliable during long coding sessions:
- Token Budget prevents context truncation mid-task
- Microcompact intelligently shrinks context window
- Fallback retries on a backup provider when primary fails
- State Machine tracks cross-turn progress
- Fork Isolation protects files from bad changes

## Install

```bash
git clone https://github.com/chunc4730-collab/hermes-agent-phase1.git
cd your-hermes-agent-repo
git am /path/to/hermes-agent-phase1/patches/*.patch
```

## Patches

| File | Layer | Description |
|------|-------|-------------|
| 0001 | L1 | Token Budget, Plan Models, Session State |
| 0002 | L2 | Conversation Loop (budget, resume, fallback, fork) |
| 0003 | L3 | Compression, Anthropic Adapter Fallback |
| 0004 | L4+L5 | Run Agent, Model Catalog, Agent Init |

## Base Version

Apply to Hermes Agent at commit ef3a650f0 (post-upstream-cherry-picks baseline).

## Pairing

These patches pair with the [hermes-coding-agent](https://github.com/chunc4730-collab/hermes-coding-agent) plugin.
The plugin runs on any Hermes, but Phase 1 makes it more stable for long tasks.

## License

MIT
