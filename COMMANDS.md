# Command Reference

`claude-mileage` (token-tengu 👺) uses a minimal command model designed to be invisible for basic use but powerful for advanced context control.

### 🧩 Interaction Commands

#### `ask <prompt> [files...]`
The primary entry point.
- **Mileage Action:** Injects local project memory, prunes provided files, and enforces "Diff-First" output for code.
- **Waste Reduction:** Warns if the context size exceeds the likely requirement for the task.

#### `plan <prompt>`
Strategy before execution.
- **Mileage Action:** Forces Claude into a low-token "Planning Mode."
- **Waste Reduction:** Prevents the "coding-by-accident" loop that burns through message limits on dead-end paths.

### 🧠 Memory & Context Commands

#### `memory [init|edit|view]`
Manage the local `.mileage/` directory.
- **Mileage Action:** Maintains the `brief.md` (project overview) and `history.log` (last actions).
- **Waste Reduction:** Replaces long cloud thread history with targeted local summaries.

#### `compact <target>`
Manual context compaction.
- **Mileage Action:** Generates a local `.summary` or `.interface` for a file or folder.
- **Waste Reduction:** Allows Claude to understand a library or module without reading every line of source.

#### `context [pin|unpin|clear]`
Session context management.
- **Mileage Action:** Persists specific files in the "pre-processor" window for the next few messages.
- **Waste Reduction:** Avoids re-pasting the same core files in a single session.

### 📊 Utility Commands

#### `budget`
Usage awareness.
- **Action:** Analyzes local logs to estimate daily/weekly token usage.
- **Waste Reduction:** Provides the visibility needed to adjust discipline before reaching limits.
