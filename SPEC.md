# Technical Specification (v1)

## 🏗️ System Architecture
`claude-mileage` (token-tengu 👺) is a local Node.js wrapper that sits between the user and the official `claude` binary. It is designed to be a "Zero-Dependency-on-API" tool—it interacts strictly with the CLI.

## 📦 Core Pipeline Components

### 1. Request Shaper (The Pre-Processor)
- **Automatic Pruning:** Uses basic heuristics (or language-specific rules) to strip comments, imports, and boilerplate from code context.
- **Prompt Injection:** Prepend local memory (`brief.md`) and append formatting instructions (e.g., "Respond only with a patch").
- **Intervention UI:** A simple CLI confirmation screen showing:
  - Estimated tokens.
  - Files included.
  - The final shaped prompt.

### 2. Local State Management (.mileage/)
A project-root directory containing:
- `brief.md`: Human/AI-maintained project overview.
- `history.log`: Compact summary of past successful steps.
- `cache/`: Local file summaries and interface signatures.

### 3. Execution Wrapper
- **Binary Call:** Spawns a child process of the official `claude` binary.
- **Stream Capture:** Pipes Claude's output back to the user while capturing it locally for the `history.log` update.

## 🛡️ Safety Boundaries
- **No Data Storage:** Prompts are prepared in memory; only summaries are saved to `.mileage/`.
- **No API Keys:** The tool relies on the user's existing authenticated Claude CLI session.
- **Explicit Consent:** No prompt is sent to Anthropic without a manual user confirmation (unless `--yes` flag is used).
