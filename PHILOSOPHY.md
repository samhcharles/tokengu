# Philosophy: The Mileage Manifesto

### 1. Discipline over Brute Force
Don't ask Claude to "fix the whole project." Ask it to fix a single function with the minimum necessary context. `claude-mileage` provides the tooling to make this surgical approach easier than the lazy one.

### 2. Stateless by Default
Thread history can be a budget trap. It grows linearly and consumes your message allotment exponentially. We prefer "stateless" messages where each prompt contains exactly what is needed for that task and nothing more. We use local files to bridge the gap between messages.

### 3. Compact Context
Context should be a curated list, not a dump. We favor diffs, interfaces, and summaries over raw source repetition. If you are referencing a 500-line file to change 5 lines, you are wasting mileage.

### 4. Local Memory
The project's architecture, recent changes, and style guides should live in local markdown files. The wrapper manages these automatically, ensuring Claude "remembers" without the user having to re-type it or rely on expensive thread history.

### 5. Transparency & Control
You should always see what is being sent before it goes. `claude-mileage` is designed to be simple on the surface for "prompt demons" but fully inspectable underneath for "CLI discipline" enthusiasts.

### 6. Respect the Platform
Anthropic provides a world-class service. We respect their Terms of Service and technical boundaries. We aim to be the most efficient guests on their infrastructure by sending the highest-signal prompts possible.
