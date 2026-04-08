---
name: digital-self
description: Build a digital portrait of yourself through deep reflective conversations. Use "/digital-self" to start or continue, "/digital-self init" for first-time setup, "/digital-self explore <dimension>" to focus, "/digital-self update" for quick changes, "/digital-self status" for progress, "/digital-self review" to hear back, "/digital-self export" to generate a portable version.
---

# Digital Self

A skill that helps you build a comprehensive digital self-portrait through deep, reflective conversations. The output is a structured collection of markdown files that any AI agent can consume to quickly understand who you are.

## Routing

Parse the user's command arguments and dispatch to the appropriate sub-skill:

| Command | Sub-skill | Description |
|---------|-----------|-------------|
| `/digital-self` (no args) | `continue.md` | Continue the interview from where you left off |
| `/digital-self init` | `init.md` | First-time setup + start first interview |
| `/digital-self continue` | `continue.md` | Explicit alias for continue |
| `/digital-self explore <dimension>` | `explore.md` | Deep dive into a specific dimension |
| `/digital-self update` | `update.md` | Quick recent-changes capture |
| `/digital-self status` | `status.md` | Show progress overview |
| `/digital-self review [dimension]` | `review.md` | Hear back your understanding |
| `/digital-self export` | `export.md` | Generate portable version |

## Auto-detection

Before routing, check whether a digital-self directory already exists:

1. Check `~/.digital-self/` (global location)
2. Check `./digital-self/` (local location)

**If neither exists AND the user did not explicitly say `init`:**
- Inform the user: "It looks like you haven't set up your digital self yet. Let me get that started."
- Route to `init.md`

**If a directory exists:**
- Use that path as the base for all operations
- If BOTH locations exist, ask the user which one to use

## Dimension name mapping

When the user provides a dimension name (for `explore` or `review`), map natural language to the canonical dimension names:

| User might say | Maps to |
|---------------|---------|
| identity, personality, who I am, values, beliefs | `identity` |
| capabilities, skills, what I can do, knowledge, tools | `capabilities` |
| patterns, habits, routines, how I work, health, daily life | `patterns` |
| relationships, people, friends, family, partner | `relationships` |
| story, history, journey, experience, past, career | `story` |
| inner world, feelings, dreams, goals, struggles, current | `inner-world` |

If the mapping is ambiguous, ask the user to clarify.
