# The Wrapper Model: How it Works

`claude-mileage` is a "Pass-Through" wrapper. It doesn't replace the official Claude CLI; it prepares the stage for it.

### The Flow
1. **Command Input:** You type `claude-mileage ask "Fix the bug in auth.ts"`.
2. **Context Assembly:**
   - The wrapper looks at `auth.ts`.
   - It reads your local `.mileage/brief.md`.
   - It prunes the file to only show the relevant lines.
3. **User Confirmation:**
   - The wrapper shows you: *"Sending brief.md + 45 lines of auth.ts. Estimated: 800 tokens. Continue? (Y/n)"*
4. **CLI Execution:**
   - Upon confirmation, the wrapper calls the real `claude` binary with the assembled prompt.
5. **Output Capture:**
   - The response is streamed to your terminal.
   - The wrapper then updates your local `history.log` with a summary of the change.

### The Dispatcher (Launcher Mode)
In launcher mode, we use a small shell script or binary named `claude` that lives earlier in your `PATH` than the official one. It checks for your preference and either:
- Executes the official binary immediately (Normal mode).
- Opens the `claude-mileage` interface.

This provides a seamless experience without breaking the underlying installation. It is entirely opt-in and reversible.
