# My AI Chief of Staff

This is a personal fork of [claude-chief-of-staff](https://github.com/mimurchison/claude-chief-of-staff), originally created by [Mike Murchison](https://linkedin.com/in/mikemurchison), CEO of [Ada](https://ada.cx). This fork is maintained by [@xtellurian](https://github.com/xtellurian) and may diverge from the upstream repo over time.

The original README describes the system well:

> Over the past few months, I've been building something on Claude Code that has fundamentally changed how I work: an AI chief of staff that connects to every tool I use, knows my priorities and relationships, and operates 24/7 in the background.

This repo gives you the same foundation. Your context, your goals, your voice.

Watch the original walkthrough and demo [here](https://x.com/mimurchison/status/2022368529417224480)

---

## What It Does

Four pillars. One system.

### 1. Communicate
Triage your inbox across email, Slack, and messaging. Get draft responses written in your voice, prioritized by who matters most. I went from 90 minutes of morning inbox processing to about 5.

### 2. Learn
Morning briefings, meeting prep, market signals — all automated. Before every meeting, Claude pulls context from every source: past emails, meeting notes, CRM data, calendar history. You walk in prepared without doing the prep.

### 3. Deepen Relationships
A personal CRM that builds itself. 160+ contacts tracked, auto-enriched every 15 minutes across all channels. Staleness alerts when important relationships go quiet. Suggested outreach with context. I never forget to follow up.

### 4. Achieve Goals
Define your quarterly objectives. Every triage decision, scheduling recommendation, and task prioritization is filtered through what you said matters most. Claude tells me when my calendar doesn't match my goals.

---

## Quick Start

### Prerequisites

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- Gmail MCP server (for email)
- Google Calendar MCP server (for scheduling)

### 3 Steps

```bash
# 1. Clone
git clone https://github.com/xtellurian/claude-chief-of-staff.git
cd claude-chief-of-staff

# 2. Install
chmod +x install.sh
./install.sh

# 3. Try it
claude
# Then type: /gm
```

First morning briefing in under 15 minutes from clone.

### Installation Notes

The installer copies template files into `~/.claude/`. It will not overwrite files that already exist — this includes `CLAUDE.md`. If you have already set up and customized your `~/.claude/CLAUDE.md`, re-running `install.sh` will leave it untouched.

---

## Features

### Morning Briefing (`/gm`)
Start every day knowing exactly what matters. Calendar, tasks, urgent messages, signals — before you open your inbox.

### Inbox Triage (`/triage`)
Scan all connected channels and get a prioritized list with draft responses.

| Tier | Action | Example |
|------|--------|---------|
| **Tier 1** | Respond NOW | Board member asking for input |
| **Tier 2** | Handle today | Customer escalation |
| **Tier 3** | FYI / archive | Newsletters, notifications |

### Task Management (`/my-tasks`)
Tasks with execution, not just tracking. Claude drafts the email, does the research, preps the document.

### Contact Enrichment (`/enrich`)
Auto-scans email, Slack, WhatsApp, calendar, and meeting notes to build rich relationship profiles. Alerts you when contacts go stale. Suggests what to talk about.

### Goal-Aligned Everything
Your `goals.yaml` is the source of truth. Claude references it constantly — triaging email, proposing meetings, scoring tasks. It pushes back when your time allocation drifts from your stated priorities.

---

## What's Included

```
claude-chief-of-staff/
├── CLAUDE.md                    # Your AI operating system — customize this
├── install.sh                   # One-command setup
├── goals.yaml                   # Quarterly objectives template
├── my-tasks.yaml                # Task tracking
├── schedules.yaml               # Automation schedules
├── contacts/
│   └── example-contact.md       # Contact file template
├── commands/
│   ├── gm.md                    # Morning briefing
│   ├── triage.md                # Inbox triage
│   ├── my-tasks.md              # Task management
│   └── enrich.md                # Contact enrichment
└── docs/
    ├── setup-guide.md           # Detailed setup walkthrough
    ├── mcp-servers.md           # MCP server installation
    └── customization.md         # Make it yours
```

---

## MCP Servers

More servers = more capability. Start with the essentials, add over time.

| Server | Required? | What It Enables |
|--------|-----------|-----------------|
| Gmail | **Yes** | Email triage, drafting, sending |
| Google Calendar | **Yes** | Scheduling, availability, meeting prep |
| Slack | Recommended | Slack triage, channel monitoring |
| WhatsApp | Optional | WhatsApp message triage |
| iMessage | Optional | iMessage triage (macOS only) |
| Granola | Optional | Meeting notes context |
| PostHog | Optional | Product analytics |

See [docs/mcp-servers.md](docs/mcp-servers.md) for installation instructions.

---

## Customization

The `CLAUDE.md` file is the core. It defines:

- **Who you are** and what you care about
- **How you write** so every draft sounds like you
- **Your goals** so Claude knows what matters
- **Your constraints** (mine: home by 5:30 for dinner)
- **Your relationships** and how to manage them

The longer you use it, the better it gets. Context compounds.

See [docs/customization.md](docs/customization.md) for the full guide.

---

## Philosophy

A few beliefs this system is built on:

1. **AI should push you, not just serve you.** A great chief of staff challenges priorities, says "no" to low-leverage work, and keeps you honest about where your time goes.

2. **Clarity beats comprehensiveness.** Fewer, clearer priorities. Explicit tradeoffs. Fast decisions with flagged assumptions.

3. **Systems compound.** Every interaction makes the system smarter. Contact notes get richer. Writing style gets more accurate. The longer you use it, the better it gets.

4. **Ship, don't polish.** Drafts should be send-ready. Outputs should be usable immediately. Bias toward closing loops.

---

## Contributing

This is a personal fork. For general improvements to the system, consider contributing to the [upstream repo](https://github.com/mimurchison/claude-chief-of-staff). For issues specific to this fork, open an issue here.

---

## Credits

Originally created by [Mike Murchison](https://linkedin.com/in/mikemurchison) ([@mimurchison](https://twitter.com/mimurchison)). Forked and maintained by [@xtellurian](https://github.com/xtellurian).

---

MIT License. See [LICENSE](LICENSE) for details.
