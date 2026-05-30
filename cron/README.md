# cron/README.md

How to set up scheduled automations for your household.

---

## What cron jobs do

Cron jobs tell Hermes to do something automatically at a set time — without you having to ask. You write them in plain English. Hermes handles the scheduling.

---

## How to add a cron job

You don't edit this file directly. Instead, tell Hermes what you want in chat:

> "Every Sunday at 6pm, ask me what I want to cook this week."

> "Every Friday at 4pm, send me a summary of what's happening next week."

> "On the 1st of every month, remind me to pay the school dinner balance."

Hermes will create the job and confirm it's running.

---

## Example jobs for a family household

| When | What Hermes does |
|------|-----------------|
| Weekdays at 7:00am | Sends morning briefing (weather, calendar, tasks) |
| Sundays at 6:00pm | Prompts weekly meal planning session |
| Fridays at 4:30pm | Sends weekly summary |
| Mondays at 8:00am | Checks for school events in the next 7 days |
| 1st of each month | Reminds about school dinner balance |
| Day before a school event | Sends a heads-up reminder |

---

## Viewing and editing jobs

To see what's scheduled: `hermes cron list`
To remove a job: `hermes cron delete [job name]`
To pause all jobs: `hermes gateway pause`
