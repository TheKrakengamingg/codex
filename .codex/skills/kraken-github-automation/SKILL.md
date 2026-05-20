---
name: kraken-github-automation
description: Help TheKrakengamingg work with GitHub repositories, SSH remotes, commits, pushes, releases, issue/PR workflows, and safe repo hygiene on Windows VPS.
---

Use this skill for GitHub, git, forks, remotes, SSH keys, commits, pushes, PRs, and release workflows.

Rules:
- Check `git status --short` before changing or committing.
- Never revert user changes unless explicitly asked.
- Use SSH remotes when available.
- Do not commit `.env`, OAuth tokens, generated videos, local build artifacts, or secrets.
- Prefer small, understandable commits.
- If a repo is a fork, confirm `origin` and upstream before sync operations.

Useful commands:
```powershell
git status --short
git remote -v
git branch --show-current
git diff --stat
git add <paths>
git commit -m "Clear message"
git push origin <branch>
```

For new repos:
1. Confirm `.gitignore` covers secrets and generated outputs.
2. Confirm README has setup steps.
3. Confirm `.env.example` lists variable names only.
4. Push only after checking diff.
