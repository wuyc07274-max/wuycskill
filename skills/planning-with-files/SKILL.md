---
name: "planning-with-files"
description: "Manus-style file-based planning for complex multi-step tasks"
---

# Planning With Files

Implements Manus-style file-based planning for complex tasks. Creates task_plan.md, findings.md, and progress.md.

## When to Use
Starting complex multi-step tasks, research projects, or any task requiring >5 tool calls.

## Core Files
- **task_plan.md** — Task breakdown and plan
- **findings.md** — Research findings and discoveries
- **progress.md** — Progress tracking

## Workflow
1. Create task_plan.md with step-by-step plan
2. Execute each step, documenting findings in findings.md
3. Update progress.md after each completed step
4. Review plan and adjust as needed

## Features
- Automatic session recovery after /clear
- Pre-tool hooks auto-read current plan
- Complex task decomposition
- Progress checkpointing
