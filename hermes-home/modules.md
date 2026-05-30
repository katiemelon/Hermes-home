# modules.md

Reference for all available household modules. Used by the AI during bootstrap to recommend which modules to enable.

---

## 🌅 Morning Briefing

**What it does:** Sends you a daily summary at a time you choose — typically covering today's weather, calendar events, your task list, and anything flagged from the previous day.

**Best for:** People who feel scattered in the morning and would benefit from a single "here's what today looks like" message before the chaos starts.

**Delivery options:** Telegram message, email, or available on request via chat.

**Pairs well with:** Cron Automations (to schedule the delivery), Kids' Schedule (to include school events), Weekly Summary.

**Skip if:** The user already has a strong morning routine and finds daily check-ins annoying.

---

## 🍽️ Meal Planning & Grocery Lists

**What it does:** Helps plan weekly meals, generates shopping lists, and can track pantry staples. Can adapt to dietary preferences, family size, and shopping habits.

**Best for:** Households where "what's for dinner?" is a daily source of stress, or where grocery trips feel disorganised.

**Notes:** Works best with a consistent weekly planning session (e.g. Sunday evening). Hermes can prompt the user to do this.

**Pairs well with:** Cron Automations (weekly meal planning reminder), Email Drafting (for click-and-collect orders).

**Skip if:** The user already has a system they love and isn't looking to change it.

---

## 🎒 Kids' School Schedule

**What it does:** Tracks term dates, school events, non-uniform days, permission slip deadlines, and other school-related calendar items. Sends reminders ahead of time.

**Best for:** Parents who regularly forget about school events until the morning of, or who manage multiple children's schedules.

**Notes:** The user will need to input term dates and events initially. Hermes can be prompted to check for upcoming events each morning.

**Privacy note:** Children's names, schools, and schedules are treated as sensitive data. Hermes will never share this information outside the household's trusted channels.

**Pairs well with:** Morning Briefing (include school events in the daily summary), Cron Automations (weekly "check ahead" reminder).

**Skip if:** The household has no school-age children, or the user already has a reliable calendar system.

---

## ✉️ Email Drafting & Sending

**What it does:** Drafts emails on your behalf — you describe what you need to say, Hermes writes it, you review and approve (or Hermes sends if you've given it permission). Can handle school emails, GP appointments, work follow-ups, etc.

**Best for:** People who procrastinate on emails, find formal writing stressful, or regularly need to send similar types of emails.

**Modes:**
- **Draft only** — Hermes writes it, you copy-paste and send yourself
- **Draft + send** — Hermes sends from your designated email address after you approve

**Pairs well with:** Gmail setup (the dedicated Hermes Gmail account from your pre-meeting prep).

**Skip if:** The user is comfortable writing emails and doesn't see this as a pain point.

---

## 📋 Weekly Summary

**What it does:** Delivers an end-of-week review — typically: tasks completed, tasks outstanding, upcoming week preview, and any notes Hermes has accumulated during the week.

**Best for:** People who like to feel on top of things but don't have time to review their week deliberately.

**Delivery:** Usually sent Friday afternoon or Sunday evening — user's choice.

**Pairs well with:** Cron Automations (scheduled delivery), Morning Briefing (the weekly summary informs Monday's briefing).

**Skip if:** The user finds weekly reviews feel like homework and won't actually read them.

---

## ⏰ Cron Automations

**What it does:** Lets you schedule Hermes to do things automatically at set times — in plain English, not code. Examples: "every Sunday at 7pm, ask me what I want to cook this week", "every Friday at 4pm, send me a summary of what's happening next week".

**Best for:** Anyone who wants Hermes to be proactive rather than waiting to be asked.

**Notes:** Cron jobs are described in plain language and stored in `~/.hermes/cron/`. The user never needs to write code or understand cron syntax — Hermes handles the translation.

**Pairs well with:** Every other module. Cron is what makes the others feel automatic rather than manual.

**Skip if:** The user explicitly only wants an on-demand assistant with no scheduled activity.

---

## Compatibility matrix

| Module | Works alone | Better with |
|--------|-------------|-------------|
| Morning Briefing | ✓ | Cron, Kids Schedule |
| Meal Planning | ✓ | Cron |
| Kids Schedule | ✓ | Morning Briefing, Cron |
| Email Drafting | ✓ | Gmail setup |
| Weekly Summary | ✓ | Cron, Morning Briefing |
| Cron Automations | Needs at least one other module | Everything |
