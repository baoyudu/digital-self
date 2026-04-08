# Digital Self

Turn yourself into a structured collection of markdown files that any AI agent can read to truly understand you.

Most AI conversations start from zero. You explain your job, your preferences, your context — over and over. Digital Self fixes this by building a persistent, evolving portrait of who you are through deep reflective conversations with an AI interviewer.

The result is a set of markdown files — your "digitalized self" — that you can drop into any AI agent's context. Instead of a stranger, you get a companion who already knows you.

## What It Produces

```
digital-self/
├── me.md                  # One-page self-portrait (the only file most agents need)
├── identity/              # Who you are: facts, personality, values, beliefs
├── capabilities/          # What you can do: skills, knowledge, tools
├── patterns/              # How you operate: habits, decisions, communication, health
├── relationships/         # Your connections: family, partner, friends, professional
├── story/                 # Your journey: timeline, turning points, growth
├── inner-world/           # Your inner life: emotions, struggles, dreams, current thoughts
└── meta/                  # Interview progress tracking
```

The directory starts as an empty skeleton. As you have conversations, the AI interviewer creates files organically based on what you actually share — no pre-filled templates, no empty placeholders.

## How It Works

The interviewer doesn't ask "What are your values?" — it asks you to make choices in concrete scenarios and draws insights from your answers. It follows your lead: if you open up about something, it goes deeper. If you're brief, it moves on naturally.

One session can be 10 minutes or 3 hours. The interviewer has no predetermined endpoint — it follows your energy and lets you enter a flow state of self-reflection.

## Install

### Claude Code (via marketplace)

```bash
# Add the marketplace (one-time)
/plugin marketplace add baoyudu/digital-self

# Install the plugin
/plugin install digital-self@digital-self
```

### Manual Install

Clone this repo and symlink the skill directory:

```bash
git clone https://github.com/baoyudu/digital-self.git
ln -s "$(pwd)/digitalized-me/skills/digital-self" ~/.claude/skills/digital-self
```

### Other Agents

The skill files are plain markdown following the [Agent Skills](https://agentskills.io) standard. Copy the `skills/digital-self/` directory into wherever your agent loads skills from.

## Usage

```bash
/digital-self              # Start or continue a conversation
/digital-self init         # First-time setup (choose storage location)
/digital-self explore <dimension>  # Deep dive: identity, capabilities, patterns,
                                   #   relationships, story, inner-world
/digital-self update       # Quick check-in for recent life changes
/digital-self status       # See your progress across all dimensions
/digital-self review       # Hear back the AI's understanding of you
/digital-self export       # Generate a portable version for other agents
```

### First Time

Run `/digital-self` — it will detect there's no existing profile and walk you through setup. You'll choose where to store your data (`~/.digital-self/` globally or `./digital-self/` locally), then the first interview begins.

### Continuing

Just `/digital-self`. The interviewer loads everything it already knows about you, checks what areas are thin, and picks up the conversation naturally.

## Design Principles

- **The process is the product.** Being deeply interviewed by an AI is itself a tool for self-discovery. The files are a bonus.
- **Depth over breadth.** One richly explored topic is worth more than ten surface-level labels.
- **Organic growth.** The directory structure adapts to you. An artist and an engineer will have very different digital selves.
- **You're in control.** Stop anytime. Skip any topic. Come back whenever.

## Compatibility

Built as a universal [Agent Skill](https://agentskills.io). Works with:
- Claude Code
- Codex CLI
- Gemini CLI
- Any agent that supports skill loading

## Community

[Discussion on linux.do](https://linux.do)

## License

MIT
