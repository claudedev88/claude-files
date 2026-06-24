# Agentforce Project Starter

A Claude Code project starter that guides you through connecting to a Salesforce org and getting fully set up for Agentforce development — through natural conversation, not documentation.

## What this is

Open this project in Claude Code and it automatically runs a guided health check. It checks everything you need, tells you what each step does and why it matters, fixes what it can, and only sends you to the browser when there's no other way. You make decisions. Claude does the work.

## What you need before you start

- [Claude Code](https://claude.ai/code) installed (`npm install -g @anthropic-ai/claude-code`)
- A Salesforce org — [get a free Developer Edition](https://developer.salesforce.com/signup)
- A terminal

That's it. Claude handles the rest.

## How to launch

```bash
cd path/to/this/project
claude
```

Claude reads this project automatically and begins the setup process.

## What Claude checks

1. Salesforce CLI installed
2. Org authenticated
3. `.gitignore` & `.env` protecting sensitive files
4. Project config file created
5. SFDX project structure initialised
6. Metadata API version (min 61.0)
7. Agentforce enabled in org
8. User permissions confirmed
9. Einstein AI credits confirmed
10. Salesforce MCP Server connected to Claude Code

Each check is narrated out loud. Claude asks before taking any action. Nothing runs silently.

## Security

**Never paste credentials into Claude chat.** Anything typed into a conversation is stored in history permanently.

Claude will never ask for:
- Consumer Keys or Secrets
- OAuth or refresh tokens  
- Passwords or security tokens
- API keys of any kind

All credentials go into `.env` only — filled in directly via a text editor. Claude reads them as environment variables so the values never appear in chat. If a credential is accidentally shared in chat, treat it as compromised and rotate it immediately.

## Project files

| File | What it is |
|---|---|
| `CLAUDE.md` | The brain — Claude reads this on every session start |
| `REFINEMENT-LOG.md` | Feedback channel — notes from live testing, version history |
| `.sf-config.json` | Claude's session memory — org details and progress (gitignored) |
| `.env` | Your credentials — never commit this (gitignored) |
| `.env.template` | Safe placeholder — shows what keys are needed |
| `.gitignore` | Protects sensitive files from source control |
| `sfdx-project.json` | Salesforce DX project config |
| `force-app/` | Your Agentforce metadata lives here |
| `docs/CLAUDE.html` | Browser-readable version of CLAUDE.md |
| `docs/setup-checklist.html` | Visual checklist — open in browser to track progress |
| `archive/` | Versioned snapshots — one folder per release |

## First time setup

1. Run `claude` in this folder
2. Follow the health check — Claude will walk you through anything missing
3. When asked for credentials, open `.env` in a text editor and fill them in directly
4. Once all 10 checks pass, you're ready to build

## Returning sessions

Just run `claude` again. Claude reads `.sf-config.json` to pick up where you left off and skips any checks that are already complete.
