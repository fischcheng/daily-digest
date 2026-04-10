# daily-digest

Summarize news sources relevant to me on intersections of AI/ML/Sustainability/Climate Action/Automation.

A scheduled Claude Code remote agent runs daily at 6 AM EDT and commits a markdown digest to `summaries/YYYY-MM-DD.md`.

## Configuration

Edit [`digest-config.json`](./digest-config.json) and push to update sources or keywords — the agent reads this file on every run, no trigger changes needed.

**To add a new source:**
```json
{
  "name": "Source Name",
  "type": "rss",
  "url": "https://example.com/feed"
}
```
Use `"type": "rss"` for RSS/Atom feeds or `"type": "api"` for JSON APIs.

**To add or remove keywords**, edit the `"keywords"` array.

**To add or rename domain groups**, edit the `"domains"` array.

## Updating the Schedule

Run `/schedule` in Claude Code from this repo directory, then choose **Update**. You can change:
- The cron schedule (e.g., different time or frequency)
- The agent prompt itself

Trigger ID: `trig_018enkKYGnh8s8cHEDVKYypf`
Manage at: https://claude.ai/code/scheduled/trig_018enkKYGnh8s8cHEDVKYypf

To delete the trigger, visit: https://claude.ai/code/scheduled

## Output

Digests are written to `summaries/YYYY-MM-DD.md`, grouped by domain:
- Sustainability & Climate
- Data Engineering & Governance
- Applied AI & Automation
