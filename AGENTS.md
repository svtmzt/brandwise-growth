# Agent instructions — Hub Lean development (approved 2026-11-09)

**Before work:** read [HubOS GOV-01](https://github.com/svtmzt/the-hub-os/issues/142) and [central Hub agent rules](https://github.com/svtmzt/the-hub-os/blob/main/AGENTS.md). These are mandatory portfolio-wide instructions, subordinate to any stricter safety requirements of this project.

- Use one canonical stable branch (normally main) and private Production until actual launch; Preview exists only to inspect changes and should be short-lived.
- Avoid creating permanent QA branches, deployments, database branches, duplicate Vercel projects, CI jobs or test accounts. Reuse isolated test fixtures; add more only for a demonstrated need.
- Every temporary environment needs an owner, issue, justification, creation date, expiry/review (normally within 7 days), quota impact and cleanup plan. At completion, remove safe-to-delete temporary resources or record the dependency blocking cleanup.
- Prefer local tests and minimal CI/deploys. No paid upgrades, uncontrolled builds or model API charges without owner approval. `[skip ci]` does not necessarily suppress Vercel deployment; verify before pushing to Vercel-linked Git repositories.
- Keep synthetic QA data separate from Production, never copy live secrets into Preview by default, and never rotate/delete production data without verified dependencies/rollback.
- Report actual PASS/FAIL/blocked status, cost effects and cleanup evidence. Exceptions must be documented and justified under GOV-01; do not lower security gates to reduce complexity.

## Product-specific note
Brandwise public repository: keep public code, marketing, and examples free of private customer credentials. Product app and internal QA may live elsewhere; never merge environments solely to simplify documentation.
