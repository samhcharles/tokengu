# claude-mileage 👺

> **Better mileage for Claude CLI workflows.**  
> An unofficial, open-source local wrapper focused on usage efficiency.

---

## ⚠️ Unofficial Community Project

This is an independent, community-built open-source tool.

- Not affiliated with, endorsed by, or supported by Anthropic
- Does not provide Claude access — you must use your own Claude CLI and account
- Does not bypass, modify, or extend usage limits
- Runs locally and prepares requests before calling the official Claude CLI

See [DISCLAIMER.md](./DISCLAIMER.md) and [TRADEMARK_NOTICE.md](./TRADEMARK_NOTICE.md) for details.

---

## The Thesis

`claude-mileage` is a local workflow wrapper for Claude CLI designed to reduce unnecessary usage and improve efficiency.

In many real workflows, usage is lost to:

- oversized context
- repeated inputs
- long, unstructured threads
- unnecessary output
- broad requests that should have been smaller tasks

This project focuses on **mileage** — getting more useful work out of the workflow you already have through better request shaping, tighter context, and local-first tooling.

> **On “Mileage over Max”**  
> This phrase is internal shorthand for an efficiency-first approach.  
> It is not a statement about Anthropic’s pricing or subscription tiers.

---

## What it is

A terminal-native workflow layer that helps structure how requests are prepared before they are sent to Claude.

It is designed to help in two ways:

### For disciplined CLI users
- keep context tighter
- reduce repeated state
- make workflows more predictable
- keep memory local and inspectable

### For users who just want it to work
- reduce waste automatically where possible
- make broad requests easier to handle
- keep normal Claude CLI workflows usable
- improve defaults without requiring constant tuning

`claude-mileage` encourages:

- **Tighter context** — send only what matters
- **Smaller tasks** — reduce failure, retries, and bloated prompts
- **Local memory** — avoid relying on long conversation history
- **Summarization** — reuse compressed information instead of raw logs
- **Focused edits** — prefer diff-first workflows for coding tasks
- **Optional launcher mode** — choose between standard Claude and mileage workflows

Everything happens locally. Your normal Claude CLI is still used for execution.

---

## How it helps

At a high level, `claude-mileage` aims to improve workflows by:

1. gathering only the context that matters  
2. compacting or summarizing large inputs  
3. reducing repeated project state across requests  
4. encouraging smaller, cleaner task boundaries  
5. keeping useful working memory on your machine  

The goal is not to change Claude itself.

The goal is to reduce waste before a request is sent.

---

## What it is not

- Not a replacement for Claude or any Anthropic service
- Not a proxy, API wrapper, or hosted tool
- Not a way to bypass limits or policies
- Not a system for accessing Claude outside official channels
- Not a multi-agent platform or automation-heavy framework

---

## Who it’s for

- Developers and terminal-first users
- People using Claude CLI in day-to-day workflows
- Users who want more predictable, efficient request flow
- People who prefer local, inspectable, hackable tools
- People who want better defaults without turning everything into a giant system

---

## Who it’s not for

- Users looking for altered limits or “unlimited” usage
- People expecting a hosted platform or GUI-first product
- Users looking for account sharing, access resale, or proxy tooling
- Teams looking for enterprise orchestration or large multi-user systems

---

## Open Source

This project is fully open source and built in public.

Contributions are welcome — especially around:

- context selection and compaction
- command design
- local memory strategies
- safe, practical defaults
- documentation and clarity

The goal is to keep the tool simple, transparent, and useful.

---

## Trademark Notice

“Claude” is a trademark of Anthropic.  
This project uses the name only to describe compatibility with Claude CLI.
