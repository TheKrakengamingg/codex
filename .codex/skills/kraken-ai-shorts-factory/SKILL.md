---
name: kraken-ai-shorts-factory
description: Work on TheKrakengamingg's AI Shorts Factory project at C:\Users\Administrator\ai-shorts-factory, including Flask UI, autopilot scheduling, ElevenLabs TTS, Pollinations visuals, ffmpeg rendering, YouTube/TikTok/Instagram uploaders, and safe API-credit controls.
---

Use this skill whenever the user asks about the AI Shorts Factory, YouTube Shorts automation, video rendering, uploader integrations, scheduled posting, or the Flask web panel.

Project facts:
- Main path: `C:\Users\Administrator\ai-shorts-factory`
- Web app: `src\web_app.py`
- Renderer: `src\shorts_factory.py`
- Autopilot: `src\autopilot.py`
- YouTube uploader: `src\youtube_upload.py`
- TikTok uploader: `src\tiktok_uploader.py`
- Instagram uploader: `src\instagram_uploader.py`
- Final videos must be named `*_final.mp4`
- Past Videos UI must only list `*_final.mp4`
- Scheduled task: `AIShortsAutopilot`
- Autopilot launcher: `run_autopilot.ps1`
- Logs: `data\autopilot.log` and `data\autopilot-task.log`

Operational rules:
- Never print API keys, OAuth tokens, or `.env` values.
- Do not run full video generation unless the user asks, because it consumes OpenAI/ElevenLabs/API credits.
- When debugging generation, prefer syntax checks, import checks, and metadata/log inspection first.
- Keep the anti-credit-drain guards: LLM retries capped, one provider selected, lock file, no startup generation loops, UI submit button lock.
- Keep final output cleanup strict: only final `.mp4` and `.json` should remain in `outputs/`.
- For YouTube uploads, default privacy is public unless the user asks otherwise.
- For Instagram, remember Graph API requires a public `video_url`; local Windows paths cannot be uploaded directly.

Common commands:
```powershell
cd C:\Users\Administrator\ai-shorts-factory
.\.venv\Scripts\python.exe -m py_compile src\shorts_factory.py src\autopilot.py src\web_app.py
Get-ScheduledTaskInfo -TaskName AIShortsAutopilot
Get-Content data\autopilot.log -Tail 80
Get-ChildItem outputs -File
```

When making changes:
1. Inspect the current file and logs.
2. Patch the smallest relevant module.
3. Run `py_compile`.
4. If `web_app.py` changes, restart the Flask process.
5. Report exact paths and whether generation/upload was actually run.
