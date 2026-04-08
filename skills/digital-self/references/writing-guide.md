# Writing Guide

Reference for the agent on how to create and update files in the digital-self directory.

## File Creation

### When to create a new file

Create a new file in a dimension directory when:
- You've gathered enough information about a focused topic to write at least 3-5 meaningful points
- The topic doesn't fit neatly into an existing file in that dimension
- An existing file is growing beyond one focused topic — split it

Do NOT create files preemptively. Only create when you have actual content to write.

### Naming conventions

- English, kebab-case: `core-values.md`, `career-journey.md`, `close-friends.md`
- Descriptive and specific: `programming-skills.md` not `skills-1.md`
- No dimension prefix: the directory already provides context (e.g., `capabilities/programming-skills.md` not `capabilities/capabilities-programming-skills.md`)

### Frontmatter format

Every file in a dimension directory must have this YAML frontmatter:

```yaml
---
title: "The human-readable title in the user's language"
dimension: identity | capabilities | patterns | relationships | story | inner-world
created: 2026-04-08
updated: 2026-04-08
---
```

### Content structure

Each file has two types of content, interleaved naturally:

**1. Structured summary** — clear, scannable points that any AI can quickly parse:

```markdown
## Key Points

- Values autonomy above financial security — has turned down higher-paying offers to maintain independence
- Identifies as an introvert but thrives in small-group deep conversations
- Strong aversion to corporate hierarchy and performative communication
```

**2. Original voice** — the user's own words, preserved in blockquotes with timestamps:

```markdown
> "I don't hate people. I hate pretending to be interested in small talk
> when there's real stuff we could be talking about."
> — 2026-04-08

> "The moment I realized I could just... leave, everything changed.
> Not that it was easy. But knowing I had the option made staying a choice."
> — 2026-04-08
```

The ratio should lean toward structured summary for everyday content, and include more original voice for emotionally significant or particularly revealing statements.

### What to mark as original voice

Preserve the user's exact words when:
- They express a strong feeling or conviction
- They tell a vivid story or specific anecdote
- Their phrasing captures something that a summary would flatten
- The way they say something matters as much as what they say

Do NOT quote mundane factual answers ("I live in Shanghai" doesn't need to be a blockquote).

## File Updates

### When to update vs. create new

- If new information adds to or refines an existing topic → update the existing file
- If new information reveals a distinct new topic → create a new file
- If an update would make a file lose its focus → split into two files

### Update mechanics

- Change the `updated` date in frontmatter
- Add new points to the structured summary
- Add new quotes to the appropriate section
- If information contradicts what was previously recorded, update it — don't keep both versions. Add a brief note: `(Updated 2026-04-08: previously thought X, but further conversation revealed Y)`

## me.md Updates

Update `me.md` after every session (at natural breakpoints during long sessions). Follow the structure in `references/me-template.md`. Key rules:

- Keep it under ~500 words (English) / ~1500 characters (Chinese)
- Write in fluent narrative, not bullet lists
- The "When Interacting With Me" section is written FOR other AI agents
- The "Learn More" section lists only files that actually exist, with one-line descriptions
- As the digital self grows, me.md should become MORE concise, not longer — distill, don't accumulate

## meta/progress.md Updates

Update after every session:

- Reassess richness level (●○ scale, 1-5) for each dimension that was touched
- Update "Content so far", "Gaps", and "Suggested direction" based on what was learned
- Update "Overall Assessment" and "Next Session Suggestion"

## meta/log.md Updates

Append a new entry after every session:

```markdown
## YYYY-MM-DD

- Duration: ~X minutes
- Dimensions covered: list of dimensions touched
- Key discoveries: 2-3 sentence summary of what was learned
- Files changed: list of created/updated files
- Emotional note: any moments of particular engagement or significance
```
