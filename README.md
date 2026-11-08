# AI readiness assessment repo

This is your private repo for the AI readiness assessment day. Only you, the
admins and the assessment tools can see it. The AI scorer sees it under your
anonymous id (dev-NN), never your name.

> **Your project: انبار دارو · PharmaStock.** The title is the whole brief: [`02-project/app/BRIEF.md`](02-project/app/BRIEF.md).

## Before the day

1. Clone this repo and check that your coding agent works in it.
2. Put screenshots of your setup in `00-setup/`: your agent, its config, any
   MCP servers you use.
3. Fill in your profile and the setup checklist on Reporter (AI Readiness
   page).

## On the day

1. Work on the project in `02-project/app/` with your AI tools, during the
   window shown on Reporter: design, plan, build, test and deliver it.
2. **Commit at least once an hour.** Commits after the window are ignored;
   your repo is frozen at your last commit inside the window.
3. **Every hour, add a progress note** to `02-project/progress/`, named
   `NN-HHMM.md` (hour number, then the time): `01-0930.md`, `02-1030.md`, …
   Start from `templates/hourly-note.md`. Each note needs at least one
   screenshot in `02-project/images/`, named `h<hour>-<what>.png`
   (`h3-tests-green.png`).
4. Add a line to `02-project/timelog.csv` for each block of work:
   `09:05,09:50,Plan,steps for the day,Claude Code + GLM-5.3,cut scope to fit`
5. **In the last hour:**
   - Copy your agent sessions into `02-project/agent-logs/`:
     `python3 tools/export-agent-logs.py --since 09:00` (use your start
     time). It covers Claude Code, Codex, OpenCode and the DeepSeek harness.
     Read the files and delete anything private. Export Cursor or web chats
     to Markdown by hand into the same folder.
   - Copy `templates/how-i-worked.md` to `02-project/how-i-worked.md` and
     fill it in (5–10 lines).
   - Fill in `SUBMISSION.md`.
   - Commit and push before the window ends.
6. Never commit passwords, API keys or `.env` files (`.env.example` is fine).
   Reporter scans every commit.

Reporter checks this repo every 15 minutes during the day and lists anything
missing on your AI Readiness page.

## Where things go

| Path | What goes there |
| --- | --- |
| `00-setup/` | Screenshots of your setup (before the day) |
| `01-profile/` | Nothing; your profile lives in Reporter |
| `02-project/app/` | Your work on the project |
| `02-project/progress/` | One note per hour, `NN-HHMM.md` |
| `02-project/images/` | Screenshots and short recordings (up to 2 min) the notes refer to |
| `02-project/agent-logs/` | Your exported agent sessions (last hour) |
| `02-project/timelog.csv` | start, end, stage, task, tool, notes |
| `02-project/how-i-worked.md` | Written in the last hour, from `templates/how-i-worked.md` |
| `SUBMISSION.md` | Filled in at the end: how far you got, what works and how to run it |
| `templates/` | Forms to copy; leave the originals as they are |
| `tools/export-agent-logs.py` | Copies your agent sessions into `02-project/agent-logs/` |

Agent setup files (`AGENTS.md`, `CLAUDE.md`, `.mcp.json`, `opencode.json`,
`.claude/`, `.opencode/`, `prompts/`, `harness/`, `evals/`) can live at the
repo root or in `02-project/app/`. Both places count.
