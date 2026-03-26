# claude-mileage 👺

<!-- BANNER_START -->
<!-- [Placeholder: Future project banner or terminal-style logo] -->
<!-- BANNER_END -->

> **Better mileage for Claude CLI workflows.**  
> An unofficial local preparation layer focused on reducing context waste and improving task discipline.

[![Status: Documentation-First](https://img.shields.io/badge/Status-Documentation--First-blue)](#roadmap)
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

### ⚠️ UNOFFICIAL COMMUNITY PROJECT
**This is an unofficial, community-driven open-source project.**
- Not affiliated with, endorsed by, or supported by Anthropic.
- Requires your own Claude account/subscription and the official Claude CLI.
- Does not bypass, circumvent, or defeat usage limits.
- See [DISCLAIMER.md](./DISCLAIMER.md) for full details.

---

## 👺 The Token-Tengu Identity
`claude-mileage` is guarded by the **token-tengu 👺**—a subtle, disciplined identity for your terminal. It represents a shift from "brute-force context" to "surgical precision." It is built for those who want to get more useful work out of the workflow they already use.

## 🛠️ How it Works
`claude-mileage` acts as a local pre-processor. It prepares your prompts, selects the right context, and compacts data **before** calling the official binary.

### The Pipeline
```text
  [ PROMPT / DIFF / FILES ]
             ↓
    ( Context Selection )  ←— Filter out boilerplate/unrelated noise
             ↓
    ( Context Compaction ) ←— Generate local summaries/interfaces
             ↓
    [   CLAUDE CLI BIN   ] ←— Official execution via your account
             ↓
  [ RESULT + MEMORY + CACHE ]
```

## 🎯 Who it is For
- **Disciplined Systems Thinkers:** Users who want local, inspectable memory, tight context control, and repeatable workflows.
- **High-Velocity Prompting:** Users who just want "smarter defaults" so the CLI handles context selection and output formatting automatically.

## ✨ Core Features
- **Stateless-by-Default:** Clears cloud thread history frequently; moves project state to local files.
- **Local Memory:** Maintains a project brief and history log in `.mileage/`.
- **Diff-First Coding:** Forces targeted patches instead of expensive full-file rewrites.
- **Context Preview:** See your token cost and selected snippets before you hit send.

## 🚀 Status & Implementation
This project is currently in its **Documentation-First** phase. We are defining the system architecture and command models before committing to the first implementation scaffold.

[View the Roadmap](./ROADMAP.md) | [Read the Creator's Note](./CREATORS_NOTE.md)

---
**Trademark Notice:** "Claude" and related marks are trademarks of Anthropic PBC. Used nominatively for compatibility description.
