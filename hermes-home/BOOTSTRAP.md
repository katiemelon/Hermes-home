# BOOTSTRAP.md

You are setting up a fresh household assistant from the hermes-home scaffold.

**This repo is not a drop-in live workspace.** Your job is to interview the user, recommend modules, and then generate tailored files under `workspace/`.

---

## Your task in order

### 1. Introduce yourself
Tell the user you'll run a short household setup interview — small batches of questions, nothing overwhelming. Estimated time: 5–10 minutes of conversation.

Example opening:
> "I'm going to ask you a few questions about your household so I can set up Hermes to actually fit your life — not a generic template. I'll go in small batches and won't ask you everything at once. Ready?"

---

### 2. Run the interview
Use `onboarding-interview.md` as your question bank.

Rules:
- Ask **2–4 questions at a time**, then wait for answers before continuing
- Do not ask all questions at once
- Skip questions where the answer is already obvious from context
- If the user seems unsure about something technical, explain it briefly and move on

---

### 3. Review modules
After the interview, consult `modules.md` and present:
- **Recommended modules** (clearly fits their household)
- **Optional modules** (might be useful, worth discussing)
- **Skipped modules** (doesn't apply — briefly say why)

Ask the user to confirm before proceeding.

---

### 4. Generate workspace files
Apply results using `apply-results.md` as your guide.

Before writing anything, present a short summary:
> "Here's what I'm about to create: [list files + brief description of each]. Does this look right?"

Wait for confirmation, then produce all files.

Files to generate:
- `workspace/SOUL.md`
- `workspace/IDENTITY.md`
- `workspace/TOOLS.md`
- `workspace/HEARTBEAT.md`
- `workspace/MEMORY.md`
- Any relevant `workspace/resources/` files for enabled modules

---

### 5. Deliver cron ideas (if applicable)
If the user enabled scheduled automations, suggest 2–4 concrete cron job ideas based on their answers. Use `cron/README.md` for plain-language format. Reference `cron/jobs.template.json` only as shape examples — do not copy IDs or specific values.

---

### 6. Close out
Tell the user:
- Which files to copy into `~/.hermes/`
- How to reload Hermes to pick up the new config
- That they can update any file at any time in plain English — they never need to touch code

---

## Output contract

Every successful bootstrap produces exactly:

| Output | Description |
|--------|-------------|
| Summary | 3–5 sentence overview of the household configuration |
| Enabled modules | List with one-line rationale each |
| Disabled modules | List with one-line reason each |
| File changes | The complete contents of each `workspace/` file |
| Cron ideas | 2–4 job suggestions (if cron module enabled) |

---

## Reference files

- Interview questions → `onboarding-interview.md`
- Module details → `modules.md`
- How to apply answers → `apply-results.md`
- Workspace file map → `primitives.md`
