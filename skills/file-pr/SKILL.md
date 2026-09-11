---
name: file-pr
description: File a concise pull request. Use when the user asks to file, open, or create a PR.
---

# File PR

Before filing, check whether a PR for this branch already exists; update it instead of opening a duplicate. Fetch and rebase onto the latest PR target branch, using the repository's default branch unless the task specifies another target. Review the diff against that branch to make sure its contents match the goal.

PR titles usually become commit messages, so follow the repository's title conventions. Look at recently merged PRs and Git history for examples.
Prefer a concise, human-readable title that explains why the change matters:

BAD:
> perf(server): negotiate permessage-deflate on the websocket

GOOD:
> perf(server): reduce websocket traffic with compression

Open the description with the actual problem, then briefly explain the final solution. Keep it aligned with the final diff as scope changes. Do not lead with an implementation inventory:

BAD:
> Removed implicit workspace carry-over from every "new thread" entry point (cmd +n / cmd+shift+o, sidebar v1/v2 buttons, command palette). New threads inherit only the project from context; branch, worktree, and env mode always come from the configured defaults. Deleted buildContextualThreadOptions, startNewThreadInProjectFromContext, and the v1 sidebar's seed-context machinery.

GOOD:
> Starting a thread from an existing worktree ignored the configured worktree preference. New threads now respect that preference.

Include numerical improvements only when supported by measurements.

End the PR description with the actual model and harness used, following this format:

**Model:** GPT-6 Astra **Harness:** Codex Desktop

Open a real PR rather than a draft so review bots run.

Merge only per the disposition given in the request (merge when green, or stop and report). If none was given, report and ask.
