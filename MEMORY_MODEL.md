# Local Memory Model

The greatest waste of tokens is "reminding" Claude what you are doing. `claude-mileage` solves this by moving state from the Cloud (Thread History) to the Local Disk (Memory).

### The `.mileage/` Folder
- `brief.md`: A 500-word overview of the project goals, tech stack, and progress.
- `history.log`: A compact, local log of every "Final Outcome" achieved in the session.
- `context.json`: A list of "pinned" files and their last-seen hashes.

### The Workflow
1. **Initialize:** `claude-mileage init` creates the brief.
2. **Update:** After every successful `ask`, the wrapper asks the user (or Claude): "Summarize this outcome for your local memory in 2 sentences."
3. **Inject:** The next `ask` prepends the `brief.md` and the last 3 entries from `history.log`.
4. **Purge:** The actual Claude thread history can be cleared frequently because the "memory" lives on your machine.
