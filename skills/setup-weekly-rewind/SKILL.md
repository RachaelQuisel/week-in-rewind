---
name: setup-weekly-rewind
description: Set up or adjust an opt-in recurring Week in Rewind Computer History recap, with optional delivery to the user's own Slack direct message. Use when the user asks to schedule, automate, repeat weekly, send to direct message to the user, change timing, or stop a recurring recap.
---

# Set up Week in Rewind

Read [the conversation and writing rules](../week-in-rewind/references/conversation-and-writing.md) before responding.

## Start the conversation

If the request has no details, ask:

1. "When should the recap run, and which time zone should it use?"
2. "Should it appear in this chat, your own Slack direct message, or both?"
3. "Which tone and focus should future recaps use? You can keep the defaults."

Wait for missing answers. Reuse a schedule or destination already supplied. For a change or stop request, identify the existing schedule before changing it. Explain missing access without creating a duplicate schedule.

Use this skill only when the user requests a recurring recap or a change to one. Installing the plugin itself creates no schedule and sends no messages.

1. Confirm the separately installed Computer History plugin is available to the local scheduled runner. Read its status. Explain a paused/stopped recorder as a possible coverage gap; do not broaden observation settings. If unavailable, report the prerequisite and leave any existing schedule intact.
2. Resolve schedule and time zone from the user's request or conversation. Ask only for a truly missing required choice. A user who gives "Friday at 4 PM Pacific" has supplied both. Use the app's `automation_update` tool for create/update/delete/view, following its schema. Do not write raw automation directives or duplicate a matching automation. Inspect existing matching automations and update one when appropriate.
3. Keep a reusable automation prompt. It must invoke the `week-in-rewind` skill; compute the preceding seven days and exact `[start, end)` interval; check Computer History status and timestamps; read six-hour summaries and verify surprising details in ten-minute summaries or raw events; cover work patterns, detours, observed shortcuts, writing style, a kind roast, and coverage gaps; never make unsupported claims or expose sensitive raw data.
4. If Slack delivery is requested, identify the connected workspace and the user's own account at setup, then resolve its direct message to the user channel. Do not place a hard-coded person, workspace, or channel in this reusable skill. The automation prompt should carry the resolved destination and require a fresh direct message to the user identity check before each send. If destination verification fails, do not send.
5. The automation prompt must check whether the exact coverage window was already delivered (using the prior delivery record or destination search). Post to the approved chat and/or Slack destination as requested, then verify the returned message or link. Only mark delivered after verification. A failed send remains retryable and must be reported accurately.
6. Keep the user's requested channel and notification preferences. A weekly recap is an explicitly requested periodic update; send it even when the observed week is quiet, while naming meaningful coverage gaps. If the user asks to stop, delete or pause the matching automation according to their wording and report the result.

For this plugin's own recap text, use [Week in Rewind](../week-in-rewind/SKILL.md). A schedule is local to the user's account and runner; plugin distribution does not copy schedules or Slack permissions to other people.
