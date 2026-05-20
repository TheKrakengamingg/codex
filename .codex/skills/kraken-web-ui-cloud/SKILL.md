---
name: kraken-web-ui-cloud
description: Build or improve practical SaaS-style web UIs, Flask/FastAPI dashboards, cloud/VPS deployments, public routes, auth, reverse proxies, domain/SSL setup, scheduled jobs, and production operations for TheKrakengamingg projects.
---

Use this skill for web panels, dashboards, public VPS apps, cloud deployment, domains, SSL, reverse proxies, and operational hardening.

Design defaults:
- Build the usable app screen first, not a marketing landing page.
- Keep operational dashboards dense, practical, and easy to scan.
- Avoid fake preview widgets unless they actually work.
- Add double-submit protection for long-running forms.
- Protect public panels with login/session auth.
- Keep visible controls mapped to backend parameters.

Backend defaults:
- Flask or FastAPI is acceptable; follow the existing project.
- Put secrets in `.env`, never in source.
- Validate upload/generation routes with auth.
- Add logs for long-running tasks.
- For background jobs on Windows VPS, prefer Task Scheduler and a `.ps1` launcher.
- Use lock files for tasks that must not overlap.

Deployment checklist:
- Confirm host/port binding.
- Confirm firewall rule if exposing a port.
- Confirm auth before exposing publicly.
- Confirm scheduled task next run and last result.
- Confirm logs are written somewhere persistent.
- Confirm generated files are not listed unless they are final deliverables.

Common Windows commands:
```powershell
Get-NetTCPConnection -LocalPort 7860
Get-CimInstance Win32_Process | Where-Object { $_.CommandLine -match 'web_app.py' }
Get-ScheduledTaskInfo -TaskName <TaskName>
Start-Process -FilePath ".\.venv\Scripts\python.exe" -ArgumentList "src\web_app.py" -WindowStyle Hidden
```
