# Resume Agent: starter kit

Build your own team of AI agents that **reviews your resume, builds one from your LinkedIn profile, matches you to any job, and finds open roles that suit you**. No coding needed: you build every agent by pasting plain-English instructions into Claude.

> 📘 **Start here:** download this kit, then open [`starter/GUIDE.pdf`](starter/GUIDE.pdf) and follow it step by step. (A text version is in [`starter/GUIDE.md`](starter/GUIDE.md).)

---

## What you'll build

You talk to one agent, the **coordinator**, by typing `/resume`. It hands the work to five specialists, each with one job:

```
                        You type /resume
                               │
                       ┌───────▼───────┐
                       │  Coordinator  │
                       └───────┬───────┘
       ┌─────────────┬─────────┼──────────┬─────────────┐
       ▼             ▼         ▼          ▼             ▼
 Profile reader  Job reader  Job finder  Reviewer      Writer
```

| Agent | What it does | Writes |
|---|---|---|
| **Profile reader** | Reads your resume or LinkedIn PDF and copies the facts exactly | `output/profile.md` |
| **Writer** | Turns those facts into a clean one-page resume; can tailor it to a job | `output/resume.html` |
| **Reviewer** | Scores your resume and suggests honest rewrites; scores you against a job | `output/review.md`, `output/match-….md` |
| **Job reader** | Reads a job posting from a link or pasted text | `output/job-….md` |
| **Job finder** | Searches for open jobs that suit you and opens every link to check it's still open | `output/jobs.md` |

**You walk away with:** a resume review, a printable one-page resume, a match report and a tailored resume for any job you choose, and a shortlist of real, open jobs.

## The rules every agent follows

1. **Never invent facts.** Your resume can be reworded and reordered, but nothing is added that you haven't done. If a job asks for a tool you don't have, it shows up in your gaps, never on your resume.
2. **Closed until proven open.** Every job link is opened and checked before you see it.
3. **Plain language.** Everything is written for a non-technical reader.
4. **Private by default.** Nothing is emailed or uploaded. Web searches use role, skills and location only, never your name, contact details or employer.

## What you need

- A paid **Claude** plan (Pro or higher) and the **Claude desktop app** (you'll use its **Code** tab)
- About **60–90 minutes**
- Your **resume as a PDF**, or your **LinkedIn profile as a PDF** (on your profile: **More → Save to PDF**)
- Two free search tools, **Parallel Search** and **Firecrawl**. The guide shows you how to add them; no account or API key is needed.

## Quick start

1. Click the green **Code** button above, then **Download ZIP**, and unzip it.
2. Open the Claude desktop app, go to the **Code** tab, and open the `starter` folder.
3. Open `starter/GUIDE.pdf` and follow Step 0 onwards.

**Just want to try the finished version?** Open the `finished` folder in Claude instead, add the two search tools (guide Step 1), drop your PDF into `finished/inbox/`, and type `/resume`.

## What's in this repo

```
starter/                  ← you build in here
  GUIDE.pdf · GUIDE.md      the step-by-step guide
  inbox/                    put your resume or LinkedIn PDF here
  output/                   the agents' work appears here
  templates/                the resume design
  samples/                  two made-up people to practise with
finished/                 ← the complete, working project (compare if stuck)
  CLAUDE.md                 the house rules
  .claude/agents/           the five specialist agents
  .claude/commands/         the /resume coordinator
```

## Guide at a glance

| Step | You build |
|---|---|
| 0 | Set up your folder and get your resume as a PDF |
| 1 | Add two free search tools (Parallel Search, Firecrawl) |
| 2 | The house rules (`CLAUDE.md`) |
| 3 | Agent 1: the profile reader |
| 4 | Agent 2: the writer, your first resume |
| 5 | Agent 3: the reviewer |
| 6 | Agent 4: the job reader |
| 7 | Match yourself to a job |
| 8 | Agent 5: the job finder |
| 9 | The `/resume` coordinator |
| 10 | Make it yours |

The guide is written for Claude Code. The same prompts can be adapted to Codex or other AI coding tools.

## Practice data

`samples/` holds two **fictional** people, Priya Raman (marketing analyst, Bengaluru) and Arjun Mehta (support lead, Pune), so you can try everything without using your own details. Their names, companies and contact details are made up.

## Privacy

Your resume is sent to Claude (Anthropic) so it can read it. The agents don't email, upload or share anything else, and your files stay in your folder. Don't commit your own resume or `output/` files if you fork this repo.
