# IBM Bob Usage Statement

IBM Bob 2.0 is the orchestration core of RepoRevive — not a bolted-on chat feature. Bob performs the audit, the planning, and the renovation itself, through five specific integration points:

1. **Full-repo audit (Inspector).** Bob runs in Agent mode pointed at the cloned repository: it navigates the file tree, reads source files, READMEs, CI configs and lockfiles using its document-understanding capability, and reasons over the entire codebase instead of isolated snippets. It returns structured findings — test coverage, dependency freshness, complexity hotspots, documentation gaps, type-safety issues, vulnerable dependencies — as a machine-readable JSON report that feeds our scoring engine.

2. **Parallel analysis via subagents.** A single Bob session spawns parallel subagents: one sweeps dependency manifests, one computes AST-based complexity metrics, one audits tests and documentation. Bob merges their outputs into a single health report, using its parallel-task orchestration to keep audits fast on large repositories.

3. **Renovation planning (Architect).** Bob consumes the audit JSON and generates a dependency-ordered, prioritized task backlog. Every task carries rationale, affected files and acceptance criteria, and is scoped small enough to be verified independently.

4. **Guided renovation (Executor + Validator).** For each task, Bob edits the code, runs builds and tests through its shell access, checks the acceptance criteria and updates the task status. A separate Validator pass reviews each diff before it is committed, and the 0–100 health score is recomputed after every merged task so the dashboard reflects progress in real time.

5. **Team development workflow.** Every team member ran Bob sessions throughout the hackathon: scaffolding the Next.js dashboard, building the six-dimension scoring engine, debugging the GitHub ingestion pipeline, generating the architecture diagram, and reviewing the final codebase. Per-member Bob session screenshots are included in the [`team/`](../team/) directory as required.

watsonx.ai / watsonx Orchestrate: not used in this build — all reasoning and agent orchestration run on IBM Bob 2.0.
