# Week in Rewind

Your week, with receipts and a wink. This plugin turns **opted-in Computer History** into a concise, funny recap of work patterns, detours, observed keyboard shortcuts, writing style, and one kind roast.

## Before you start

- Requires the separately installed **Computer History** plugin and access to its local history on a supported Mac. Week in Rewind does not record activity or broaden observation settings.
- Ask for a recap with `Use $week-in-rewind to recap my last seven days.` For an on-demand recap, it asks three quick, silly questions about genre, roast heat, and what to spotlight. Answer in one line or say “surprise me.” A shorter or more serious tone is fine: `... roast level 0` or `... roast level 3`.
- For optional scheduling, ask `Use $setup-weekly-rewind to send this to my own Slack DM every Friday at 4 PM Pacific.` A connected Slack account is required for Slack delivery. The setup skill must verify the destination is your self-DM and avoid duplicate schedules.
- Installation alone does not create an automation or send a message.

## What you get

The recap is a small story with evidence behind it: a few plotlines, one side quest if there was one, a keyboard award only when a shortcut was observed, a note on writing style only when the evidence supports it, and a silly, warm roast sentence. You can react, correct a detail, or ask it to change the tone; it will revise the recap while keeping the evidence straight. It calls out meaningful gaps in the recorded period. It does not score productivity or diagnose personality.

Scheduled recaps use the default playful tone and do not ask questions, so they can arrive on time.

Raw Computer History events can contain sensitive text. The skill reads only what's needed, keeps personal or third-party details out of the recap, and shares nothing externally unless you request a destination. Computer History remains the source of truth for its own capture and retention settings.

## Distribution notes

This package contains skills only. It does **not** bundle the proprietary Computer History recorder or grant access to another person's history. A recipient must install and enable Computer History separately. Scheduled recaps require a local runner with Computer History available at run time; Slack delivery requires that recipient's own connected workspace and self-DM. Public directory eligibility and cross-surface availability need separate validation.

The two skills are in [`skills/week-in-rewind/SKILL.md`](skills/week-in-rewind/SKILL.md) and [`skills/setup-weekly-rewind/SKILL.md`](skills/setup-weekly-rewind/SKILL.md).
