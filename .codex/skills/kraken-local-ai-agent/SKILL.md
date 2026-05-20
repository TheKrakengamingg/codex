---
name: kraken-local-ai-agent
description: Customize this Codex fork or similar AI coding agents with AGENTS.md rules, local skills, OpenAI/Claude/OpenRouter/Ollama providers, WSL2/Rust build setup, terminal workflows, and safe tool behavior.
---

Use this skill when the user wants to make their own Codex-like local coding agent, change this Codex fork, add skills, configure local models, or build agent tooling.

Key facts for this fork:
- Fork path on VPS: `C:\Users\Administrator\codex`
- Remote: `git@github.com:TheKrakengamingg/codex.git`
- Official source is Rust-based under `codex-rs`.
- Official build instructions expect macOS/Linux or Windows via WSL2.
- Native Windows shell currently has Node/pnpm, but may not have Rust/Cargo.

Training/customization layers:
- `AGENTS.md`: durable repo behavior rules.
- `.codex/skills/<name>/SKILL.md`: specialized procedural knowledge.
- Config/provider setup: model and authentication.
- Code changes: only when behavior cannot be handled with instructions/config.

Good first customizations:
- Branding and default prompts.
- Skills for the user's projects.
- Safer defaults for shell execution and secrets.
- Cloud/VPS workflows.
- GitHub automation skills.
- Local model provider notes for Ollama/LM Studio.

Do not promise that the fork can contain the same model weights or hidden system behavior as a hosted assistant. Be clear: we can customize tools, rules, skills, UI, and model provider, not clone a proprietary model.
