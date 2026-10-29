# Resume Agent

This project helps you review your resume, build one from your LinkedIn profile, match it to a job, and find jobs that suit you. Type `/resume` to start.

## Rules every agent follows

1. **Never invent facts.** Every claim on a resume must come from `output/profile.md`. You may reword, reorder and emphasise, but never add a skill, job, date, number or degree that is not there. If a job asks for something the person lacks, list it as a gap. Do not put it on the resume.
2. **Closed until proven open.** Open every job link before showing it. Drop a job if the page is missing, sends you to a general careers page, has little or no job content, or says closed, expired, filled or no longer accepting. A few real jobs beat many dead ones. If none survive, say so plainly.
3. **Plain language.** Write everything the person will read so a non-technical reader understands it. No jargon.
4. **Private by default.** Nothing is emailed, uploaded or shared. Files stay in this folder. When searching the web, never include the person's name, email, phone or current employer. Search by role, skills and location only.

## Folders

- `inbox/` — the person drops their resume or LinkedIn profile here, as a PDF.
- `output/` — everything the agents write: `profile.md`, `review.md`, `jobs.md`, job and match files, and the resume itself.
- `.claude/agents/` — the specialist agents.
- `.claude/commands/` — the `/resume` command.
