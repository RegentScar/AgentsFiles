---
name: file-pr
description: File a concise pull request (GitHub) or merge request (GitLab). Use when the user asks to file, open, or create a PR or MR.
---

# File PR / MR

"PR" and "MR" mean the same thing here. Pick the tool from the `origin` remote: GitHub → `gh pr …`; GitLab → `glab mr …`.

Before filing, check whether a PR/MR for this branch already exists (`gh pr list --head <branch>` / `glab mr list --source-branch <branch>`); update it instead of opening a duplicate. Fetch and rebase onto the latest target branch, using the repository's default branch unless the task specifies another target. Review the diff against that branch to make sure its contents match the goal.

PR/MR titles usually become commit messages, so follow the repository's title conventions. Look at recently merged PRs/MRs and Git history for examples.
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

Open a real PR/MR rather than a draft so review bots and pipelines run. On GitLab, pass `--remove-source-branch` unless the repository says otherwise.

Merge only per the disposition given in the request (merge when green, or stop and report). If none was given, report and ask. On GitLab, check the pipeline with `glab ci status` / `glab mr view`, and remember that `glab mr merge` enables auto-merge by default: pass `--auto-merge=false` unless auto-merge was asked for, since a merge may deploy.
