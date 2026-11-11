---
name: clipready-video
description: Turn an idea or research into a short talking-head video plan (script, hooks, beats and sources) and send it to the ClipReady iPhone app to record. Use when the person asks for a ClipReady video, a 30, 60 or 90 second video plan, or to see or send their ClipReady drafts.
---

# Make a video plan for ClipReady

Use this when the person wants to make a short vertical video (30, 60 or 90 seconds) they will record themselves in the ClipReady app.

The tools come from the ClipReady connector bundled with this plugin. The first time, the person connects it: Claude opens the ClipReady sign-in page, and they type a code from the ClipReady iPhone app (Settings, Connect an AI agent, Get a code).

1. Agree the topic, the length and who it is for. If they gave their own words or notes, keep their wording.
2. Write the script: what they will say, out loud, in plain sentences. Never invent personal experiences, results, quotes or numbers. Every number or name must come from the person or from a source you will attach.
3. Call `start_clipready_video` with the title, length and script.
4. For each fact that needs proof, find a public page that states it and call `attach_sources_to_clipready_video` with the URL and a short note of the fact. Use the returned receiptId on that fact's beat.
5. Write the plan and call `set_clipready_plan`: 4 beats for 30 s, 6 for 60 s, 8 for 90 s. Each beat's scriptSpan is copied exactly from the script, in order, covering all of it; each point is a short spoken cue. Add 1-3 hooks made of the script's own words; the first is the one shown. A hook is the reason to want the explanation, not the start of it: open on the tension (what changed, what it costs, what most people get wrong), say it straight to the viewer in one sentence of about 16 words or fewer, and skip warm-ups ("so", "today I want to"), news-first openers and hype words. Give the options different angles, not three rewordings. If the tool lists problems, fix all of them and call it again.
6. Call `preview_clipready_video` and show the person the hook and beats. Fix anything it flags.
7. Only when the person says to send it, call `send_clipready_video`. Tell them it is waiting in the ClipReady app on the home screen, under Waiting for you (Plans from your agent). They can delete a plan there by holding it.

ClipReady never records, exports or posts from here, and nothing here costs anything or offers upgrades. If the person asks to buy or upgrade something, say that isn't available here and carry on with the video.
