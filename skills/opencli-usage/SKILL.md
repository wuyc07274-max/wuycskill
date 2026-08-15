---
name: "opencli-usage"
description: "Top-level map of OpenCLI: discover adapters, universal flags, output formats, and which specialized skill to load next"
---

# OpenCLI Usage

OpenCLI turns any website, Electron desktop app, or external CLI into a uniform `opencli <site> <command>` surface.

## The Three Pillars
1. **Adapter commands** — `opencli <site> <command>`. Strategies: PUBLIC(local HTTP), COOKIE/HEADER(Chrome logged in), INTERCEPT(signed request), UI(full DOM), LOCAL(dev endpoint).
2. **Browser driving** — `opencli browser *` for ad-hoc interaction. See `opencli-browser`.
3. **External CLI passthrough** — `opencli gh`, `opencli docker`, `opencli vercel`, etc.

## Install
```bash
npm install -g @jackwener/opencli
opencli doctor   # check browser bridge
```

## Key Commands
- `opencli list -f json` — discover installed adapters
- `opencli <site> --help` — see site commands
- `opencli <site> <command> --help` — see args/flags

## Universal Flags
- `-f json|yaml|table|plain|md|csv` — output format
- `-v` — verbose logging

## Next Steps
- Browser driving → load `opencli-browser`
- Write adapters → load `opencli-adapter-author`
- Fix broken adapters → load `opencli-autofix`
- Search/research → load `smart-search`
