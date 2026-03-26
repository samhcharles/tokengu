# Technical Specification (v1)

## System Architecture
`claude-mileage` acts as a middleware between the user and the `claude` binary. It intercepts commands, processes context, and manages local state before forwarding the final payload to the official CLI.

## Install Modes
1. **Side-by-Side:** The user runs `claude-mileage <command>`.
2. **Launcher Mode (Opt-in):** The `claude` command is replaced by a dispatcher. When run without arguments, it shows a picker:
   - `› Claude (Normal)`
   - `  Claude Mileage`
   - This mode preserves the original binary path for easy rollback.

## Core Components
### 1. Context Pipeline
- **Pruning:** Automatically removes comments, docstrings (if requested), or unrelated functions from code snippets.
- **Preview:** Shows a token estimate and a "context summary" before the user hits Enter.
- **Rules:** Applies `CONTEXT_RULES.md` to every outbound message.

### 2. Local Memory Model
- Stores "Project Briefs" and "Last Action" summaries in a `.mileage/` directory.
- Injects relevant snippets into the prompt to replace long-term thread history.

### 3. Compaction Engine
- Converts raw file content into "Compact Reps" (e.g., just the function signatures).
- Encourages `diff` output instead of full file rewrites.

## Behavioral Guardrails
- **Refuse Bloat:** If a user tries to send more than X files, warn them and suggest a `compact` command first.
- **No-Retry Policy:** Discourage mindless "try again" prompts. Force a "What changed in your intent?" prompt instead.

## Output Contract
All outputs from `claude-mileage` should be:
- Minimal (fewest tokens possible to convey the answer).
- Formatted for immediate local use (e.g., clean diffs).
- Summarized at the end for the local memory log.
