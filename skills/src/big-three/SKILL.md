---
name: big-three
description: Daily focus system. Each morning the user commits to the two or three big things that will actually move their business or goals; check-ins during the day; a Friday report of committed versus done, and a month-end report. Use when the user types /big-three, asks for their morning commitment, a check-in, or a weekly or monthly focus report.
---

# Big Three

By Lior Pozin. A long to-do list feels productive. Most of it is a shopping list.
This skill measures only the two or three big things that would actually move the business.

Small tasks still get done. They just stop counting.

## The idea

A deadlift works around 70% of your body. One compound lift does the job of three or four
small exercises. Work runs the same way: one task that is big in substance beats a whole
list of small ones, even when it takes less time.

## Modes

Pick the mode from what the user says. If it is unclear, look at the time of day and the log.

### 1. Morning commit
Ask one simple question:

> What are the two or three things you commit to doing today?

Then push on them, briefly:
- If an item is small or routine, like emails, a meeting, or "follow up", ask what bigger thing it serves, and offer to swap it.
- If there are more than three, ask which ones to cut.
- Each item should be finishable today, or have a clear "done for today" line.

Log the final list with today's date.

### 2. Check-in
Run up to three times a day. Ask: what moved on each of today's big things? What is blocking?
Keep it short. If something is stuck, ask for the one next action that unblocks it.

### 3. End of day
Mark each item: done, partly done, or not done, with one line on why.
Anything not done does not roll over automatically. Tomorrow morning the user decides again.

### 4. Friday report
Show the week as a table: date, committed, done.
Then:
- **Score:** big things done out of big things committed.
- **Pattern:** which kind of item keeps slipping, and the likely reason.
- **One adjustment** for next week.

### 5. Month-end report
Same as Friday, across the month: the big things completed, the completion rate, and the
two or three items that slipped most often.

## The log

Keep a running log in this format:

```
## 2026-10-13
1. <big thing> - done / partly / not done - <one line>
2. <big thing> - ...
3. <big thing> - ...
```

- If you can read and write files, as in Claude Code, keep it in `big-three-log.md`.
- In the Claude app, work inside one Claude Project so the log lives in one place. At the end of
  each session, output the updated log in a single block and ask the user to keep it in the
  Project's files.

## Tone

Direct and brief, like a good chief of staff. No lectures. No productivity tips.
Measure only the big things.

## Optional: make it come to you

To get the morning question automatically, schedule a daily task that runs `/big-three`
in the morning, three check-ins during the day, and the report on Friday.
