---
name: "opencli-autofix"
description: "Automatically fix broken OpenCLI adapters when commands fail"
---

# OpenCLI AutoFix

Automatically fix broken OpenCLI adapters when commands fail.

## Safety Boundaries
- AUTH_REQUIRED (exit 77) — STOP, tell user to log in
- BROWSER_CONNECT (exit 69) — STOP, run `opencli doctor`
- CAPTCHA — STOP
- Max 3 repair rounds

## Workflow
1. Collect trace: `opencli <site> <command> --trace retain-on-failure`
2. Read `summary.md` (has `adapterSourcePath`)
3. Analyze failure (SELECTOR/EMPTY_RESULT/API_ERROR/TIMEOUT/PAGE_CHANGED)
4. Explore live site with `opencli browser`
5. Patch adapter at `adapterSourcePath`
6. Verify: `opencli <site> <command>`
7. If passed, file upstream GitHub issue

## Before Repair
"Empty" ≠ "Broken" — retry with alternative query, spot-check in Chrome, look for soft 404s.

## Common Fixes
- Selector update: `.old-class` → `.new-class`
- API endpoint: `/v1/old` → `/v2/new`
- Response schema: `data.results` → `data.data.items`
