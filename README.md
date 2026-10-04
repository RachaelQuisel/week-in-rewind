# Week in Rewind

Receive a short recap of your recorded computer activity. Choose the dates, tone, and focus. The recap can include supported work patterns, other activities, keyboard shortcuts, writing habits, and a kind roast.

Start with `/week-in-rewind:week-in-rewind`. The plugin asks up to three questions about missing choices. It waits for your answers. You can say "use the defaults" to choose the last seven days and a gentle roast. You can correct a detail or ask for a revision.

## Requirements

Install Computer History separately and make its local history available on a supported Mac. Week in Rewind reads that history. It does not capture activity or change recording settings. If the history is unavailable, it explains the gap and stops the recap.

## Scheduled recaps

Use `/week-in-rewind:setup-weekly-rewind` to request a recurring recap. Supply the time, time zone, and destination. The setup asks only about missing choices and checks for an existing schedule.

A scheduled run uses saved settings and asks no live questions. It needs a local runner with Computer History available at run time. Slack delivery requires your connected workspace and your own direct message. The plugin checks for prior delivery of the same period and verifies each send.

## Data and permissions

Computer History can contain sensitive text. The plugin reads the selected period and checks evidence needed for specific claims. It excludes sensitive personal and third-party details from the recap. External delivery requires your request. Computer History controls its own recording and retention settings.

The package contains two skills. It does not include the Computer History recorder, an existing schedule, or access to someone else's history. Installing it does not create a schedule or send a message. Directory listing and behavior in other apps require separate checks.

Read [how it works](Week-In-Rewind-HowItWorks-2026-10-03.md).

## License

MIT. See [LICENSE](LICENSE).
