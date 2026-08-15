---
name: "opencli-browser"
description: "Drive a real Chrome window via OpenCLI — inspect, fill forms, click flows, extract data"
---

# OpenCLI Browser

Drive a real Chrome window via OpenCLI — inspect pages, fill forms, click through logged-in flows, or extract data ad-hoc.

## Prerequisites
```bash
opencli doctor   # must be green before anything works
```

## Mental Model
1. **Selector-first target contract** — every interaction takes a numeric ref or CSS selector
2. **Every envelope reports `matches_n` and `match_level`** (exact/stable/reidentified)
3. **Compact output first, full payload on demand**
4. **Structured errors** — branch on `error.code`

## Critical Rules
1. Always inspect before acting: run `state` or `find` first
2. Prefer numeric ref over CSS once acquired
3. Read `match_level` after every write
4. Use `compound` field for form controls
5. Chain with `&&` in a single shell

## Key Commands
- `browser state` — snapshot with refs
- `browser find --css <sel>` — CSS query
- `browser click/type/select <target>`
- `browser get text/value/attributes <target>`
- `browser network` — API capture
- `browser extract` — long-form content
- `browser screenshot [path]` — viewport PNG

## Compound Form Controls
- Date: `{control, format, current, min, max}`
- Select: `{control, multiple, current, options[], options_total}`
- File: `{control, multiple, current, accept}`
