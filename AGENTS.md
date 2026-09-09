# Coding preferences - general

- Keep things simple. Channel "YAGNI" energy unless told otherwise.
- Write code, comments, documentation, commit, and pull request messages in English.
- Type safety is useful; take advantage of it.
- Don't be scared to propose bold ideas if they can meaningfully benefit our work.
- Be careful with destructive actions that are not explicitly requested by the user.
- Tests are good! Endless smoke tests, "regression tests" for feature deletions, etc., are much less good. Tests should be focused.
- Comments are a great way to clarify functionality and how code is used. Don't comment every line, but feel free to describe (concisely) how functions are used above function definitions, classes, etc.
- Keep comments up to date! When making changes, it's important to keep things in sync.

# Coding preferences - TypeScript

- Avoid `any`. Prefer inferred types.
- Avoid one-line functions that are just casting wrappers.

# Match ceremony to the task

- Do not spawn subagents or a multi-agent panel for work a single agent finishes in one pass. Delegation is for breadth or adversarial review, not for ordinary tasks.
- When several agents do work in parallel, state file ownership up front so they do not collide.

# Visual and design work

- Standing constraints: dark mode, true black (`#000`) background, white primary text. Information-dense, no decorative card/pill chrome, no light-gray subtitle lines above sections. Minimal copy. No em dashes.
- Avoid continuously repainting CSS animations (pulse, shimmer, blur, spinners); they peg the GPU on high-refresh displays.

# Blast radius

- Do not modify production, live databases, or daily-driver build/preview channels unless explicitly told to. Before accessing any of them, name the target and intended action.
