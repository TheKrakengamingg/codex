---
name: kraken-predictive-analytics
description: Build proactive analytics for TheKrakengamingg projects using user counts, FiveM server load, traffic sources, uptime, job logs, conversion data, and trend detection to forecast issues and recommend optimization before failures happen.
---

Use this skill for dashboards, metrics, prediction, anomaly detection, server load forecasting, growth tracking, retention, traffic source analysis, or proactive maintenance.

Goal:
- Move from reactive fixes to proactive operations.
- Use historical data to predict busy periods, lag risks, content performance, and conversion drops.

Useful data sources:
- FiveM player counts by time/day.
- Server CPU/RAM/network and resource tick times.
- Script error logs and restart/crash events.
- Website traffic sources and page conversion events.
- YouTube/TikTok/Instagram video metrics.
- Discord joins, applications, whitelist submissions, purchases, and retention.

Analysis patterns:
- Compare by hour of day and day of week.
- Detect recurring spikes, drops, and lag windows.
- Correlate content posts with traffic/server joins.
- Flag anomalies, not just averages.
- Recommend specific actions before peak windows.

Output style:
- Start with the prediction or risk.
- Include evidence: data window, baseline, current change, confidence.
- Recommend 1-3 concrete actions.
- Never invent metrics. If data is missing, specify what to collect next.

Example:
`Grand Kraken, Sunday 19:00-22:00 is 30% above baseline. Optimize these three FiveM resources before the next peak: ...`
