# primitives.md

Reference: the official Hermes workspace file map.

This file documents what each workspace file does in the Hermes Agent system. Use it to understand where to put information and what each file controls.

---

## Core workspace files

All live at `~/.hermes/` on the user's server.

| File | Purpose | Updated by |
|------|---------|-----------|
| `SOUL.md` | Assistant personality, tone, and hard rules | User / bootstrap |
| `IDENTITY.md` | Household context — who lives here, their shape and needs | User / bootstrap |
| `TOOLS.md` | Active channels, enabled modules, connected services | User / bootstrap |
| `HEARTBEAT.md` | Daily/weekly rhythm — when things happen | User / bootstrap |
| `MEMORY.md` | Persistent facts Hermes should always know | Hermes (auto) + bootstrap |

---

## Supporting files

| Location | Purpose |
|----------|---------|
| `~/.hermes/.env` | API keys and tokens (never put these in workspace files) |
| `~/.hermes/config.yaml` | Core Hermes configuration |
| `~/.hermes/cron/` | Scheduled job definitions |
| `~/.hermes/sessions/` | Conversation history |
| `~/.hermes/logs/` | Hermes activity logs |
| `~/.hermes/skills/` | Custom skill folders |
| `~/.hermes/memories/` | Auto-generated memory store |

---

## File loading behaviour

- Workspace files are loaded fresh at the start of each conversation — no restart needed after editing
- `SOUL.md` is loaded on every message — changes take effect immediately
- `MEMORY.md` is merged with Hermes' auto-generated memory store
- Files can be edited in plain text at any time

---

## Upstream reference

Canonical Hermes documentation: [https://hermes-agent.nousresearch.com](https://hermes-agent.nousresearch.com)
