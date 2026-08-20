# AI Interactive Learning Prompt

Turn any AI model into an instructor who teaches you one module at a time — and refuses to move on until you say you're ready.

## The problem

Ask an AI to "teach me Terraform" and you get 3,000 words with forty commands in it. You skim it, feel productive, and remember nothing by Thursday.

That's not teaching. That's a content dump.

## What this does

You give it a topic. It asks how you want to learn and how long you've got. It builds a schedule, shows it to you for approval, then teaches module by module:

**concept → why it matters in production → worked example → hands-on lab → verify your output → "ready to continue?"**

Then it stops and waits. Every time.

## Quick start

1. Open Claude, ChatGPT, Gemini or any capable model
2. Copy [`prompt.md`](prompt.md) and paste it in
3. Replace `[TOPIC]` with whatever you're learning
4. Answer the intake questions
5. Approve the plan
6. Learn

Works best in a model with a long context window, since the session builds cumulatively.

## Learning modes

| Mode | Use it when |
|---|---|
| From scratch / deep dive | You've never touched it and want proper foundations |
| Refresher | You've done this before and need it back |
| Super-fast refresher | You have an interview or meeting soon |
| Hands-on | Minimum theory, maximum labs |
| Interview prep | Concepts, likely questions, and how to tell the story |
| Enterprise-grade | Production patterns, scale, failure modes |

Timeframes: a few hours, one day, one week, one month, or custom.

## Student controls

Type any of these mid-session:

| Command | What it does |
|---|---|
| `next` | Move to the next module |
| `deeper` | Go deeper on what we just covered |
| `slower` | Break the last module into smaller pieces |
| `skip` | Skip this module, you already know it |
| `quiz me` | Test everything covered so far |
| `recap` | Summarise progress |
| `lab only` | Skip theory, go straight to hands-on |
| `interview me` | Switch to interview questions on the material |
| `plan` | Show the remaining schedule |

## The rules that make it work

Everything else is decoration. These are the load-bearing parts:

- **One module per message.** Never a full course dump.
- **Every message ends by asking if you're ready.** Then it stops.
- **Never move on from a broken lab.** Debug it with you first.
- **Labs stack.** Module 4 builds on what you made in Module 3.
- **Wrong answers get corrected directly.** Better now than in an interview.

## Where this came from

I built this while working through my own upskilling program — Terraform, Docker, Kubernetes, ArgoCD, CI/CD, AWS. Real labs, real breakages. Somewhere in there I stopped asking AI for information and started making it run a classroom.

Sessions in [`examples/`](examples/) are real, unedited.

## Contributing

Fork it and make it better. Things worth adding:

- New modes — certification prep, exam cram, teach-back mode
- Non-technical adaptations — languages, finance, music theory
- Model-specific tuning
- Example sessions from topics not covered yet

Open a PR or an issue with what you changed and why.

## Licence

MIT. Use it, change it, ship it.

---

Built by [Deepak](https://www.linkedin.com/in/cdeepak-uk/) · notes at [cicdtrail.com](https://cicdtrail.com)
