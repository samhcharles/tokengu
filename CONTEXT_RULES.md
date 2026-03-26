# Context Rules

To maximize mileage, the wrapper follows these rules when preparing context:

1. **Hierarchy of Information:** 
   - 1. User Intent (Current Message)
   - 2. Local Memory (Project Brief)
   - 3. Minimal Code/Data required for the task.
2. **Prune the Passive:** Remove non-essential code (imports, boilerplate) unless explicitly requested.
3. **Diffs > Files:** When discussing changes, always provide the "before" as a small snippet and ask for a "patch" as the "after."
4. **Summary over Raw:** If a file has been discussed before, use its local summary instead of the full text.
5. **Clear Termination:** End every prompt with a specific instruction on output format to prevent "chatter" (e.g., "Respond only with the code block").
