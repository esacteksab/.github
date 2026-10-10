---
mode: agent
---

Review all open Dependabot PRs in this repository.

Use the repository's Dependabot review workflow to:

1. List every open Dependabot PR for this repo.
2. Check CI status for each PR.
3. Read the PR body and changelog details to understand what changed.
4. Categorize each update by risk: low, medium, or high.
5. For any major version bump on a runtime dependency, investigate the migration guide and grep the codebase for affected imports and API usage.
6. Call out required code changes or behavior changes even if CI is green.
7. Group related dependency updates to avoid version mismatches.
8. Recommend whether each PR should be approved, flagged for human review, or deferred.
9. If there are multiple PRs, suggest the merge order and whether any remaining PRs should be rebased.

Output a concise table with:

- PR number
- package name and version change
- dependency type
- risk level
- CI status
- action

Use the following risk legend:

- 🟢 Low
- 🟡 Medium
- 🔴 High

If a PR appears high-risk, explain the specific migration or behavioral risk and name the files or code patterns likely affected.
