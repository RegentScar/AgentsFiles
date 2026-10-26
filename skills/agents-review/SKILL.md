---
name: agents-review
description: Launches an independent subagent to review all changes. Use when the user asks for an agents review, an independent review, or a subagent to review the changes.
---

# Agents Review

Spawn an independent subagent (Agent tool, `general-purpose`) to review all changes made so far. Do not do the review yourself.

1. **Scope:** Collect everything that changed: staged, unstaged, and untracked files plus commits on the current branch (`git status`, `git diff`, `git log <base>..HEAD`). Without git, list the files changed in this session.
2. **Brief:** Give the agent a self-contained prompt: the goal of the change, the files/commits to review, and the instructions below. Do not pass along your own reasoning or conclusions; the reviewer should judge the code fresh.
3. **Reviewer instructions:**
   - Read the full diff and enough surrounding code to understand the context and all callers.
   - Look for bugs, regressions in existing behavior, broken callers or contracts, unhandled edge cases, error-handling gaps, security issues, and missing or broken tests.
   - Run the relevant tests, build, or lint if available.
   - Do not modify any files.
   - Report only real issues, each with `file:line`, what is wrong, a concrete failure scenario, and severity. Say clearly if nothing was found.
4. **Verify:** Check each reported finding yourself and drop false positives. Present the confirmed findings to the user, most severe first.
