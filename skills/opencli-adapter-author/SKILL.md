---
name: "opencli-adapter-author"
description: "Write OpenCLI adapters for new sites or add commands to existing sites"
---

# OpenCLI Adapter Author

Guide for writing an OpenCLI adapter for a new site or adding a new command to an existing site.

## Goal
From zero to passing `opencli browser verify` within 30 minutes.

## Prerequisites
- `opencli doctor` passes
- Data visible in browser (resolve auth first if not)
- Data is HTTP/JSON/HTML format

## Workflow
1. Read site memory (`~/.opencli/sites/<site>/endpoints.json`, `notes.md`)
2. Site recon (`opencli browser analyze <url>`)
3. API discovery (network capture → state extraction → bundle search → token → intercept)
4. Direct endpoint verification (must get 200 + non-empty data)
5. Field decoding (self-explanatory keys / known conventions / decode playbook)
6. Design columns per `output-design.md`
7. Write adapter: `opencli browser init <site>/<name>`, copy similar adapter, modify
8. Verify: `opencli browser verify <site>/<name>`
9. Generate fixtures: `--write-fixture`, tighten patterns
10. Confirm field values match what's on the page
11. Write back site memory (endpoints/field-map/notes/fixtures)

## Key Rules
- Adapter imports only `@jackwener/opencli/registry` + `@jackwener/opencli/errors`
- `columns` array must align 1:1 with `func` return object keys (including order)
- Use typed errors from `references/typed-errors.md`
- Debug dumps only in `~/.opencli/sites/<site>/fixtures/` or `/tmp/`
