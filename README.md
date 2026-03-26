# claude-mileage 👺

> **Better mileage for Claude CLI workflows.**  
> An unofficial, open-source local wrapper focused on usage efficiency.

---

### ⚠️ Unofficial Community Project

**This is an independent, community-built open-source tool.**

- Not affiliated with, endorsed by, or supported by Anthropic  
- Does not provide Claude access — you must use your own Claude CLI and account  
- Does not bypass, modify, or extend usage limits  
- Runs locally and prepares requests before calling the official Claude CLI  

See [DISCLAIMER.md](./DISCLAIMER.md) and [TRADEMARK_NOTICE.md](./TRADEMARK_NOTICE.md) for details.

---

## The Thesis

`claude-mileage` is a local workflow wrapper for Claude CLI designed to reduce unnecessary usage and improve efficiency.

In many workflows, usage is lost to:
- oversized context
- repeated inputs
- long, unstructured threads
- unnecessary output

This project focuses on **mileage** — getting more useful work out of the usage you already have through better workflow discipline.

> **On “Mileage over Max”**  
> This phrase is internal shorthand for an efficiency-first approach.  
> It is not a statement about Anthropic’s pricing or subscription tiers.

---

## What it is

A terminal-native workflow layer that helps structure how requests are prepared before they are sent to Claude.

It encourages:

- **Tighter context** — send only what matters  
- **Smaller tasks** — reduce failure and retries  
- **Local memory** — avoid bloated conversation history  
- **Summarization** — reuse compressed information instead of raw logs  
- **Focused edits** — diff-first workflows for code  
- **Optional launcher mode** — choose between standard Claude and mileage workflows  

Everything happens locally. Your normal Claude CLI is still used for execution.

---

## What it is not

- Not a replacement for Claude or any Anthropic service  
- Not a proxy, API wrapper, or hosted tool  
- Not a way to bypass limits or policies  
- Not a system for accessing Claude outside official channels  

---

## Who it’s for

- Developers and terminal-first users  
- People using Claude CLI in day-to-day workflows  
- Anyone who wants more predictable, efficient usage patterns  
- Users who prefer local, inspectable tools  

---

## Who it’s not for

- Users looking for automation-heavy or agent-based systems  
- People expecting unlimited usage or altered limits  
- GUI-first workflows or platform-style tools  

---

## Open Source

This project is fully open source and built in public.

Contributions are welcome — especially around:
- context selection and compaction  
- command design  
- local memory strategies  
- documentation and clarity  

The goal is to keep the tool simple, transparent, and practical.

---

**Trademark Notice:**  
“Claude” is a trademark of Anthropic.  
This project uses the name only to describe compatibility with Claude CLI.
