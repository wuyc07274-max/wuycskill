---
name: "notebooklm"
description: "Query Google NotebookLM notebooks for source-grounded, citation-backed answers"
---

# NotebookLM Research Assistant Skill

Interact with Google NotebookLM to query documentation with Gemini's source-grounded answers. Each question opens a fresh browser session, retrieves the answer exclusively from your uploaded documents, and closes.

## When to Use
User mentions NotebookLM, shares a NotebookLM URL, wants to query docs, or uses phrases like "ask my NotebookLM".

## Critical: Always Use run.py Wrapper
NEVER call scripts directly. ALWAYS use `python scripts/run.py [script]`.

## Core Workflow
1. Check auth: `python scripts/run.py auth_manager.py status`
2. Authenticate if needed: `python scripts/run.py auth_manager.py setup`
3. Manage notebooks: `python scripts/run.py notebook_manager.py list/add/search/activate`
4. Ask questions: `python scripts/run.py ask_question.py --question "..." [--notebook-id ID]`

## Follow-Up Mechanism (CRITICAL)
Every answer ends with "Is that ALL you need?" — analyze gaps and ask follow-ups before responding to user.

## Smart Add
When user wants to add a notebook without details, query it first to discover content, then add with proper metadata.

## Key Commands
- `python scripts/run.py notebook_manager.py list` — List notebooks
- `python scripts/run.py ask_question.py --question "..."` — Ask question
- `python scripts/run.py auth_manager.py status` — Check auth

## Limitations
- No session persistence
- 50 queries/day on free accounts
- Manual doc upload required
