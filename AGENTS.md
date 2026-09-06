# Coding preferences - general

* Keep things simple. Channel "YAGNI" energy unless told otherwise.
* Type safety is useful; take advantage of it.
* Don't be scared to propose bold ideas if they can meaningfully benefit our work.
* Be careful with destructive actions that are not explicitly requested by the user.
* Tests are good! Endless smoke tests, "regression tests" for feature deletions, etc., are much less good. Tests should be focused.
* Comments are a great way to clarify functionality and how code is used. Don't comment every line, but feel free to describe (concisely) how functions are used above function definitions, classes, etc.
* Keep comments up to date! When making changes, it's important to keep things in sync.

# Coding preferences - TypeScript

* Avoid `any`. Prefer inferred types.
* Avoid one-line functions that are just casting wrappers.

# Match ceremony to the task

* Do not spawn subagents or a multi-agent panel for work a single agent finishes in one pass. Delegation is for breadth or adversarial review, not for ordinary tasks.
* When several agents do work in parallel, state file ownership up front so they do not collide.

# Visual and design work

* Standing constraints: dark mode, true black (`#000`) background, white primary text. Information-dense, no decorative card/pill chrome, no light-gray subtitle lines above sections. Minimal copy. No em dashes.
* Avoid continuously repainting CSS animations (pulse, shimmer, blur, spinners); they peg the GPU on high-refresh displays.

# Blast radius

* Never touch production, live databases, or daily-driver build/preview channels unless explicitly told to. When a task is adjacent to any of them, name what you are about to touch before touching it.

# Pull Requests

* Make sure titles follow conventions from the repo. They should be simple and easy to understand. Use conventional commit styles in projects that use them, i.e., "fix(web): new threads no longer spike CPU".
* PR descriptions should aim for simplicity. Open with a minimal, clear description of the problem. Follow up with how you solved it.
* Add a blurb to the end of the PR description about what model and harness is making the changes.
* **Open a real PR**, not a draft. Drafts do not get review-bot coverage.
* **Rebase onto latest `main` before opening.** Stale branches conflict and waste a review round.
* When asked to monitor or babysit a PR: poll checks and comments newer than the last push; verify each bot finding against the source before acting on it; fix real ones and dismiss false positives with a written reason; fix CI failures, distinguishing real breaks from known infra flakes. If nothing is new, stay quiet; do not post filler comments. Stop when the repo's review bots are green on the latest commit.
* Merge only per the disposition given in the request (merge when green, or stop and report). If none was given, report and ask.
