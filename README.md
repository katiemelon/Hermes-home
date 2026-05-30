# 🏠 hermes-home

**A household scaffold for [Hermes Agent](https://hermes-agent.nousresearch.com) by Nous Research.**

Run a capable, private AI assistant that manages your family's daily life — from morning briefings to meal planning to school reminders — all from your own server.

Adapted from Claire Vo's Tradclaw but for hermes
> Maintained by [Katie](https://github.com/katie) · Built for real families, not just tech people.

---

## What this is

`hermes-home` is a starter scaffold for setting up Hermes as a **household manager**. It is not a drop-in live workspace. It's a structured interview + configuration template that shapes Hermes to your specific family's needs.

Think of it like this:
- **Hermes** is the engine
- **hermes-home** is the configuration that tells it how to run *your* household

---

## What you get

| Module | What it does |
|--------|-------------|
| 🌅 Morning Briefing | Daily summary of weather, calendar events, and tasks |
| 🍽️ Meal Planning | Weekly meal suggestions, grocery list generation |
| 🎒 Kids' Schedule | School dates, reminders, term calendars |
| ✉️ Email Drafting | Draft and send emails on your behalf |
| 📋 Weekly Summary | End-of-week household review |
| ⏰ Cron Automations | Scheduled tasks in plain English |

Not every module is right for every household. The BOOTSTRAP interview figures out which ones make sense for you.

---

## How to use this repo

**You do not edit the files yourself.** Instead, you paste one prompt into Hermes (or Claude), and it interviews you and generates your personal workspace files.

### Step 1 — Have Hermes installed and running
Follow the [setup guide](https://hermes-agent.nousresearch.com) first.

### Step 2 — Start the bootstrap interview
Open a chat with Hermes (or Claude) and paste:

```
Read the hermes-home scaffold at https://github.com/YOUR_USERNAME/hermes-home and set up my household workspace. Start with hermes-home/BOOTSTRAP.md — follow the read order, interview me, recommend modules, and generate my workspace/ files.
```

### Step 3 — Copy your workspace files
The AI will produce tailored versions of the files in `workspace/`. Copy them into your Hermes home directory at `~/.hermes/`.

---

## Repo structure

```
hermes-home/
├── README.md                    ← you are here
├── AGENTS.md                    ← rules for AI agents working in this repo
│
├── hermes-home/                 ← scaffold & interview logic
│   ├── BOOTSTRAP.md             ← start here (AI setup runbook)
│   ├── onboarding-interview.md  ← interview questions the AI asks you
│   ├── apply-results.md         ← how the AI turns answers into config files
│   ├── modules.md               ← module descriptions & compatibility notes
│   └── primitives.md            ← reference: Hermes workspace file map
│
├── workspace/                   ← template files (AI fills these in for you)
│   ├── SOUL.md                  ← assistant personality & household rules
│   ├── IDENTITY.md              ← who you are, your family, your context
│   ├── TOOLS.md                 ← which tools & channels are enabled
│   ├── HEARTBEAT.md             ← daily/weekly rhythm config
│   ├── MEMORY.md                ← what Hermes should always remember
│   └── resources/
│       └── templates/           ← blank resource files per module
│
├── cron/
│   ├── README.md                ← plain-English cron guide
│   └── jobs.template.json       ← example scheduled job shapes
│
└── skills/                      ← optional add-on skill folders
```

---

## Principles

- **No leaking family data** — Hermes never shares information about your children or household outside trusted channels. This is a hard rule, not a preference.
- **Ask before acting** — when in doubt about something sensitive, Hermes asks you first.
- **Plain English first** — all config is written in natural language, not code.
- **Modular** — only enable what you actually need. A simpler setup is a better setup.

---

## Credits & licence

Scaffold structure inspired by [tradclaw](https://github.com/ChatPRD/tradclaw) by ChatPRD.  
Hermes Agent is MIT licensed by [Nous Research](https://nousresearch.com).  
This scaffold is maintained by Katie and is free to use, fork, and adapt.
