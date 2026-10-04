## Trigger

- The user asks for a recap, requests a recurring recap, or changes an existing schedule. A configured schedule can start a later run.

## Inputs

- The dates define the recorded period.
- The tone, roast level, focus, and exclusions guide the recap.
- The separately installed Computer History plugin supplies recorded activity and coverage information.
- For scheduling, the time, time zone, destination, and available local runner define future delivery.

## What happens

1. For an on-demand recap, the plugin asks up to three missing questions about dates, tone, and focus. It waits for answers unless the user explicitly chooses defaults.
2. For scheduling, it asks for missing timing, destination, and recap preferences. It inspects existing schedules to avoid duplicates.
3. It checks Computer History access and recording status. If access is unavailable, it explains the gap and stops the recap. It preserves recording settings.
4. It reads the period summaries. It checks shorter summaries or relevant events before making a specific claim. Missing recordings do not establish inactivity.
5. It prepares observations about supported work patterns, other activities, shortcuts, and writing. It adds a kind roast only when requested and supported. It excludes sensitive details.
6. An on-demand result appears in the chat. A scheduled run uses saved settings and asks no live questions.
7. For requested Slack delivery, it verifies that the destination is the user’s own direct message. It checks for prior delivery of the same period, sends once, and verifies the message. A failed send remains unresolved.
8. A correction causes the plugin to recheck the evidence and revise the result. A stop request changes the matching schedule and reports what changed.

## Outputs

- A recap with the exact period and material recording gaps.
- A saved schedule when requested, with its configured destination.
- A verified message in an authorized destination when sending succeeds.
