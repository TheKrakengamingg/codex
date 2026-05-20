---
name: kraken-stream-automation
description: Build system automation and API integrations for TheKrakengamingg using C#, Streamer.bot, FiveM/GTA RP servers, OBS WebSocket, ElevenLabs, TTS, overlays, event triggers, and multi-step action chains.
---

Use this skill for Streamer.bot, OBS, FiveM, C# scripting, Twitch/YouTube stream automation, ElevenLabs live voice actions, overlays, or game-server-triggered content.

Design goals:
- Build complete action chains, not isolated snippets.
- Prefer clear event flow: trigger -> validation -> API call -> OBS/Streamer.bot action -> log/result.
- Keep secrets in Streamer.bot globals, `.env`, or config files; never hardcode API keys.
- Add retry limits and timeouts for external APIs.
- Log enough context to debug failed actions without leaking tokens.

C# guidance:
- Use async HTTP calls for APIs such as ElevenLabs or webhooks.
- Validate payloads before sending them to OBS or game server endpoints.
- Keep actions idempotent when possible, especially donation/sub/chat commands.
- Return readable status messages for Streamer.bot action logs.

OBS WebSocket guidance:
- Treat scene names, source names, and filter names as config.
- Common operations: switch scene, show/hide source, set text source, play media source, toggle filter, set browser source URL.
- Do not assume OBS is connected; handle connection errors.
- Keep timing explicit for multi-step overlays.

FiveM / RP server guidance:
- Respect server security: validate player identifiers and never trust client-side events blindly.
- For HTTP endpoints/webhooks, add shared-secret validation.
- For RP automations, preserve gameplay fairness and avoid actions that can be abused by chat.

Example action chain shape:
1. Streamer.bot receives Twitch/YouTube event.
2. C# action validates user/event.
3. Action calls ElevenLabs or local TTS.
4. OBS WebSocket shows overlay/source and plays audio.
5. Optional webhook notifies FiveM server.
6. Action logs success/failure and cleans temp files.
