# Philosophy: The Mileage Manifesto

### 1. Discipline over Brute Force
Don't ask Claude to "fix the whole project." Ask it to fix a single function with the minimum necessary context. `claude-mileage` provides the tooling to make this surgical approach easier than the lazy approach.

### 2. Stateless by Default
Thread history can be a trap. It grows linearly and consumes your budget exponentially. We prefer "stateless" messages where each prompt contains exactly what is needed for that task and nothing more. We use local files to bridge the gap between messages.

### 3. Compact Context
Context should be a curated list, not a dump. If you are referencing a 500-line file to change 5 lines, you are wasting mileage. We favor diffs, interfaces, and summaries over raw source.

### 4. Local Memory
The project's architecture, recent changes, and style guides should live in local markdown files (e.g., `CONTEXT.md`). The wrapper should automatically inject these when relevant, ensuring Claude "remembers" without the user having to re-type it or rely on thread history.

### 5. Transparency
You should always see what is being sent before it goes. No hidden "system prompts" that eat your tokens without your knowledge. 

### 6. Respect the Platform
Anthropic provides a world-class service. We respect their Terms of Service, their billing models, and their technical boundaries. We aim to be the most "polite" and efficient guests on their infrastructure.

> **Note on "Mileage over Max":** This phrase represents our focus on efficiency-first workflow design. It simply frames our goal: to help users get the most utility out of their messages by reducing waste.
