---
name: kraken-security-ops
description: Handle security-sensitive tasks for TheKrakengamingg projects: API keys, OAuth tokens, .env files, public VPS services, upload credentials, webhook secrets, and avoiding accidental credential leaks.
---

Use this skill whenever work touches secrets, `.env`, OAuth, API keys, public services, auth, uploads, or deployment exposure.

Rules:
- Never print secret values back to the user.
- If the user pasted a token in chat, avoid repeating it and recommend rotation if it may be exposed.
- Keep `.env` out of git.
- Use `.env.example` with variable names only.
- For public dashboards, require auth before exposing routes.
- For generated files, avoid exposing directory listings unless protected.
- For upload integrations, log status and IDs, not tokens.
- For OAuth, store tokens in `secrets/` and ensure `.gitignore` covers them.

Checks:
```powershell
git status --short
git check-ignore .env secrets\youtube_token.json
rg -n "sk-|EAAV|OPENAI_API_KEY|ELEVENLABS_API_KEY|ACCESS_TOKEN" .
```

When adding new integrations:
1. Add env names to `.env.example`.
2. Load secrets via environment variables.
3. Fail clearly when required secrets are missing.
4. Keep upload modules opt-in unless the user asks for automatic posting.
