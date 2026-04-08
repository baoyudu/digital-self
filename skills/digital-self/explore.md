---
name: digital-self:explore
description: Deep dive into a specific dimension of the digital self
---

# Digital Self — Explore Dimension

The user wants to focus on a specific dimension. The dimension name is provided as an argument (e.g., `/digital-self explore identity`).

## Valid dimensions

`identity`, `capabilities`, `patterns`, `relationships`, `story`, `inner-world`

If the user provided an unrecognized dimension name, suggest the closest match from the list above. If they said something like "values" or "personality", map it to the appropriate dimension (both → `identity`). If they said "goals" or "dreams", map to `inner-world`.

## Step 1: Load context

1. Read `me.md` for overall context
2. Read ALL files in the specified dimension directory — you need to know exactly what has already been explored
3. Read `meta/progress.md` — look at the gaps and suggested direction for this dimension
4. Skim files in other dimensions for context that might relate

## Step 2: Read reference guides

Read `references/questioning-guide.md` and `references/writing-guide.md`.

## Step 3: Start the focused conversation

Acknowledge the focus area naturally, then dive in with a situational question:

> "Let's go deeper on [dimension in natural language]. Looking at what I already know about you in this area, I'm curious about [specific gap or follow-up]..."

**Key differences from `continue`:**

- You have a clear focus dimension, so you can be more deliberate about depth
- Still follow natural tangents — if the user's answer bridges to another dimension, follow it briefly, then gently steer back
- Use what you know from OTHER dimensions to craft better questions about THIS one (e.g., if exploring `capabilities` and you know from `story` that they had a career change, ask how their skills shifted during that transition)

## Step 4: Write at breakpoints, end with review

Same behavior as `continue.md` — write at natural breakpoints, end with holistic review when the user stops.

For the holistic review in explore mode, focus the portrait on the explored dimension but reference how it connects to the broader picture.
