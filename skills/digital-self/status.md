---
name: digital-self:status
description: Display the current state of the digital self — dimension richness, last update, suggested next steps
---

# Digital Self — Status

Show the user an overview of their digital self profile. No conversation — pure information display.

## Step 1: Load data

1. Read `meta/progress.md`
2. Read `meta/log.md` — get the date and summary of the most recent session
3. Count the total number of files across all dimension directories
4. Read `me.md` — get the session count from the header

## Step 2: Display

Present a clean overview:

```
Digital Self — Status
=====================

Last session: {date from most recent log entry}
Total sessions: {N from me.md header}
Total files: {count across all dimensions}

Dimension Overview:
  identity      ●●●○○  Basic facts and personality sketched; values need depth
  capabilities  ●○○○○  Only job-related skills mentioned
  patterns      ●●○○○  Work style captured; daily rhythms unclear
  relationships ●●○○○  Partner mentioned; friends and family sparse
  story         ●●●●○  Rich career narrative; childhood untouched
  inner-world   ●●○○○  Current focus known; deeper aspirations unexplored

Suggested next: {from progress.md "Next Session Suggestion"}
```

Adapt the format to be readable. Use the actual data from progress.md — the above is just an example of the layout.

## Step 3: That's it

Don't start an interview. Don't ask questions. Just display the status and wait for the user's next action.
