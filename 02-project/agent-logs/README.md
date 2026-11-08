# Agent logs

In the last hour, copy the day's agent sessions here:

    python3 tools/export-agent-logs.py --since 09:00

Use your start time. The script reads Claude Code, Codex, OpenCode and
DeepSeek harness sessions that ran inside this repo, hides likely secrets
and writes one Markdown file per session. Read the files and delete anything
private before you commit.

Other tools (Cursor, web chats): export the conversation to Markdown by hand
and save it here, one file per session.
