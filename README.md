# ClipReady for Claude

ClipReady is an iPhone app for recording short talking-head videos. This plugin lets Claude turn an idea or your research into a recording plan and send it to the app, where you record it beat by beat. The app trims, captions and finishes the video on your phone.

## What Claude can do with it

- Write a 30, 60 or 90 second video plan from your idea, notes or research: the script, a few hooks and a beat-by-beat plan.
- Attach public pages as sources. ClipReady opens each one, checks that it states the fact, and captures a screenshot the video can show.
- Check the plan in code: every beat matches the script and every number has a source.
- Show you a preview, then send the plan to your ClipReady app when you say so.

Claude can only create and send video plans. It cannot see your recordings or anything else on your phone, and nothing is recorded, exported, posted or bought from chat.

## Install

In Claude Code:

```
claude plugin marketplace add remoteree/clipready-claude-plugin
claude plugin install clipready@clipready
```

In Claude (web, desktop or mobile) you can add the connector on its own: Settings, Connectors, Add custom connector, with the URL `https://clipready.reebuilds.org/mcp/public`.

## Connect

1. The first time Claude uses ClipReady, a sign-in page opens.
2. On your iPhone, open ClipReady and go to Settings, then Connect an AI agent.
3. Tap Get a code and type it on the sign-in page.

You can disconnect at any time in the same screen of the app.

## Try it

- "Turn my notes into a 60 second ClipReady video."
- "Make a 30 second video plan about this news, with sources."
- "Show my ClipReady drafts."

After you send a plan, it is waiting in the ClipReady app on the home screen, under Waiting for you.

## What is in this repository

- `.mcp.json`: the ClipReady connector (a remote MCP server with OAuth sign-in).
- `skills/clipready-video`: the steps Claude follows to write, check and send a plan.

## Support and privacy

- Support: https://clipready.reebuilds.org/support
- Privacy policy: https://clipready.reebuilds.org/privacy
- Terms: https://clipready.reebuilds.org/terms
