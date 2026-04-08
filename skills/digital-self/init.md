---
name: digital-self:init
description: Initialize a new digital-self profile — creates directory structure and starts the first interview
---

# Digital Self — Initialize

You are starting a new digital-self profile for the user. This is likely their first interaction with the digital-self system.

## Step 1: Choose language

Ask the user which language they'd like to use:

> "First, which language would you like me to use for our conversations and your digital self files?"
>
> **1)** 中文
> **2)** English
> **3)** 日本語
> **4)** 한국어
> **5)** Español
> **6)** Français
> **7)** Other (please specify)

Wait for the user's answer. Use the chosen language for all subsequent conversations and file content. Directory and file names always stay in English.

## Step 2: Choose storage location

Ask the user where to store their digital self:

> "Where should I store your digital self?"
>
> **A)** `~/.digital-self/` — A global location, accessible from any project. Any AI agent can find it regardless of where you're working.
> **B)** `./digital-self/` — In the current directory. More private — only accessible when you're in this project.

Wait for the user's answer. Store the chosen path as `{BASE_PATH}` for all subsequent operations.

## Step 3: Create directory structure

Create the following directories and files:

```
{BASE_PATH}/
├── me.md
├── identity/
├── capabilities/
├── patterns/
├── relationships/
├── story/
├── inner-world/
└── meta/
    ├── progress.md
    └── log.md
```

**Initial `me.md`:**

```markdown
# About Me

> Last updated: {today's date} | Based on 0 interview sessions

(This file will be populated as we get to know each other.)
```

**Initial `meta/progress.md`:**

```markdown
# Interview Progress

> Last updated: {today's date}

## Dimension Status

### identity
- Richness: ○○○○○
- Content so far: Not yet explored
- Gaps: Everything
- Suggested direction: Start with basic facts and current life situation

### capabilities
- Richness: ○○○○○
- Content so far: Not yet explored
- Gaps: Everything
- Suggested direction: Will emerge naturally from identity and story conversations

### patterns
- Richness: ○○○○○
- Content so far: Not yet explored
- Gaps: Everything
- Suggested direction: Will emerge naturally from daily life conversations

### relationships
- Richness: ○○○○○
- Content so far: Not yet explored
- Gaps: Everything
- Suggested direction: Let people come up naturally in conversation

### story
- Richness: ○○○○○
- Content so far: Not yet explored
- Gaps: Everything
- Suggested direction: Will emerge naturally as the user shares experiences

### inner-world
- Richness: ○○○○○
- Content so far: Not yet explored
- Gaps: Everything
- Suggested direction: Too early — build trust first through lighter topics

## Overall Assessment

Brand new profile. No information collected yet.

## Next Session Suggestion

Start with warm, low-pressure questions about current life situation. Follow the icebreaker approach in the questioning guide.
```

**Initial `meta/log.md`:**

```markdown
# Interview Log

(Sessions will be recorded here as they happen.)
```

## Step 4: Orientation

Tell the user exactly this, once:

> "Everything's set up. Here's how this works: we'll have a conversation — I'll ask you questions, you answer however feels natural. There are no right or wrong answers. I'm just trying to understand who you are."
>
> "You can stop anytime — just say so. Next time, use `/digital-self` to pick up where we left off."
>
> "Ready? Let's start."

## Step 5: Begin first interview

Now conduct the first interview session. Read `references/questioning-guide.md` for your questioning strategy and `references/writing-guide.md` for how to record what you learn.

**For the first session specifically:**
- Start with the "First session (init)" opening from the questioning guide
- Stay with lighter topics initially: current life situation, daily routines, what they do for work, what they do for fun
- Let deeper topics emerge naturally — don't force depth in the first 10 minutes
- As trust builds and the user opens up, follow the thread wherever it leads

**During the session:**
- At natural breakpoints (when a major topic has been thoroughly explored), silently write accumulated information to the appropriate dimension files following the writing guide
- Update `me.md` to reflect what you've learned so far
- Do NOT announce file writes — this breaks conversational flow

**When the user says they want to stop:**
1. Provide a holistic review: describe in a few paragraphs your understanding of who they are so far. This should feel like being truly seen — it's the emotional payoff.
2. Ask if your understanding is accurate, let them correct anything
3. Do a final file write: update all dimension files, `me.md`, `meta/progress.md`, and append to `meta/log.md`
4. End warmly: "I'm looking forward to our next conversation."
