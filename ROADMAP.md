# Roadmap

The path to a disciplined, high-mileage CLI workflow.

## 🟢 Phase 1: Minimal Scaffold (Now)
*Goal: Establish the wrapper plumbing and local memory.*
- [x] Vision, Philosophy, and System Design.
- [ ] Basic CLI skeleton (Node.js/TS).
- [ ] `.mileage/` directory initialization.
- [ ] "Pass-through" mode: Intercept intent → Call official `claude` binary.

## 🟡 Phase 2: Core Mileage (Next)
*Goal: Implement context selection and request shaping.*
- [ ] Context Pruning: Basic comment/boilerplate stripping.
- [ ] The "Pre-Send" Confirmation UI (Token estimation + Summary).
- [ ] "Diff-First" prompt injection for code tasks.
- [ ] Local Memory injection: Automatically prepend `brief.md` to `ask`.

## 🟠 Phase 3: Advanced Compaction (Later)
*Goal: Local summarization and language awareness.*
- [ ] `compact` command for manual folder/file summarization.
- [ ] Language-specific rules (TS, Python, Go) for interface extraction.
- [ ] Opt-in "Launcher Mode" (Binary dispatcher).
- [ ] Usage tracking and local budget dashboard.

## ⚪ Phase 4: Integrations (Future)
- [ ] Editor hooks (VS Code, Zed) for local memory sync.
- [ ] Advanced "Tengu" heuristics for automated task chunking.
