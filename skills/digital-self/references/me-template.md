# me.md Structure Reference

This is the structure reference for the `me.md` core summary file. The agent should follow this structure when creating and updating `me.md`.

## Template

```markdown
# About Me

> Last updated: {date} | Based on {N} interview sessions

{One paragraph core portrait — who this person is, what life stage they're in,
what drives them. This should read like a warm, perceptive friend describing
someone they know well. Not a resume, not a clinical profile.}

## Basic Info

{Brief facts in a compact format:}
- Name/nickname: {value}
- Age range: {value}
- Location: {value}
- Occupation: {value}
- Family: {value}
- Languages: {value}

## My Core

{A few paragraphs about what drives this person, what they value most,
where their boundaries are, and what inner conflicts they carry.
Written as narrative, not bullet points. This section should feel like
it captures the essence of the person.}

## Current State

{What's occupying them right now — professionally, personally, emotionally.
What they're focused on, what's weighing on them, what they're excited about.
This section changes most frequently.}

## When Interacting With Me

{Written explicitly FOR other AI agents. Practical guidance:}
- Communication style preferences (direct? gentle? analytical?)
- Things to avoid (triggers, pet peeves, unwanted behaviors)
- What works well (approaches, formats, tones that resonate)
- Relevant habits or patterns (e.g., "thinks out loud", "needs time to process")

## Learn More

{Dynamic list — only include files that actually exist:}
- `identity/core-values.md` — What matters most and why
- `story/career-journey.md` — The path from X to Y
- ...
```

## Guidelines

1. **Tone:** Warm but not sycophantic. Perceptive but not clinical. Like a thoughtful friend writing about someone they understand well.

2. **Length:** ~500 words (English) / ~1500 characters (Chinese). This is a hard ceiling. If you need to add something, take something out or compress.

3. **Evolution:** After the first session, me.md may only have "Basic Info" and a rough "My Core". That's fine. It grows naturally — don't fill sections with guesses.

4. **The "When Interacting With Me" section** is the most practically useful part for other agents. Invest effort here. Be specific: not "prefers clear communication" but "likes direct answers without hedging; gets impatient with excessive caveats".

5. **Language:** Write in the user's language. Section headers can stay in English for cross-agent compatibility, or be translated — follow the user's preference.
