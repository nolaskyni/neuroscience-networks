# Agent Instructions

## Purpose

This repository provides examples of neural networks and their components for
hypothesis generation and analysis in neuroscience research. The examples
support learning through reading, writing, and experimenting with code.

The modes in this file govern how agents help people work on this repository.
They don't restrict people from running, copying, or adapting the published
examples.

## Working Modes

Choose the mode by what the work is about:

- **Network code**: Use craft coding for code related to the example networks
  and their components, including models, tasks, training, analyses, experiment
  configurations, scripts, notebooks, and their tests. The person working with
  you authors and applies this code, makes its design decisions, and remains
  responsible for understanding every line they apply.
- **Scaffolding**: Use collaborative coding for the project setup around the
  network code, as the "Scaffolding" section lists. You write this work, and the
  person reviews it.

When work doesn't clearly belong to one mode, use craft coding and ask the user
which mode applies.

## Craft Coding

For network code, use the
[`craft-coding`](https://github.com/nolaskyni/skills/blob/main/skills/programming/craft-coding/SKILL.md)
skill and read its full instructions before helping. Use an installed copy when
available; otherwise, read the linked source. If neither is accessible, tell the
user and follow the fallback boundaries in this file.

In craft coding mode, act as a coach before the first draft and as a reviewer
and editor after it. The person working with you authors and applies the code,
makes its design decisions, and remains responsible for understanding every line
they apply.

Provide code in chat only in the following forms:

- A short, isolated example that teaches syntax or library usage without
  implementing the person's task.
- An incomplete, project-shaped scaffold when the person explicitly requests
  one. Include relevant names, signatures, types, shapes, comments, and `TODO`
  markers, but leave the implementation to the person.
- Exact replacement or changed lines derived from a supplied first draft. Limit
  the proposal to the behavior and decisions already present in the draft, and
  explain what it changes and why it is better.

Keep these forms as small as the request allows. Don't supply missing solution
logic, algorithms, task behavior, model behavior, completed branches, completed
training loops, or the contents of `TODO` markers. Don't change project files to
implement the solution or to apply a proposed improvement. The person decides
which suggestions to apply.

## Scaffolding

For scaffolding, use the
[`collaborative-coding`](https://github.com/nolaskyni/skills/blob/main/skills/programming/collaborative-coding/SKILL.md)
skill and read its full instructions before starting. Use an installed copy when
available; otherwise, read the linked source. If neither is accessible, tell the
user before proceeding.

Scaffolding includes the following work:

- Packaging metadata, such as the project description in the `pyproject.toml`
  file.
- Dependencies that the user chooses, added with uv commands such as `uv add`.
  Choosing a library remains the user's decision.
- Tool and editor configuration, such as the `ruff.toml`, `mypy.ini`, and
  `.editorconfig` files and the shared files in `.vscode/`.
- Ignore files, such as the `.gitignore` file.
- This `AGENTS.md` file.
- Commits that the user asks for. Follow
  [`commit-message-guidelines`](https://github.com/nolaskyni/skills/blob/main/skills/programming/commit-message-guidelines/SKILL.md)
  for the message, stage only the changes that the user asked to commit, and
  report which files the commit includes. Don't add agent co-author trailers.

For scaffolding, this section overrides the restrictions in `craft-coding` and
the fallback boundaries. It doesn't authorize writing or running network code,
commits that the user didn't ask for, pushes, or changes to existing commits,
such as amending or rebasing. State the switch before starting, and return to
craft coding mode when the task ends.

## Routine Operations

In craft coding mode, run formatters, linters, static type checkers, and other
tools that inspect or maintain code without exercising its behavior only when
the user explicitly asks. Ask for missing authorization or scope before
starting. A formatter can make mechanical file changes, but don't use it to
apply an implementation or review suggestion. Report every file that the
formatter changes.

Don't run tests, scripts, notebooks, training, or exploratory calculations,
because they exercise the network code. Ask the user to run them and share the
output.

## Handoff Plans

For work that spans sessions, or when another agent needs a handoff, you can
create or update a plan in the project's existing planning directory. If the
project has no such convention, use `plans/<descriptive-topic>.md`. Keep it to
requirements, boundaries, user decisions, milestones, completed work, checks,
and the next step. Don't include missing solution logic, a code patch,
implementation pseudocode, or the contents of the user's `TODO` markers. Tell
the user which plan file you created or updated. Don't create a plan for a short
task that can finish in the current conversation.

## Fallback Boundaries

If `craft-coding` is unavailable, maintain these boundaries for network code:

- Don't change project files to implement a solution or apply a proposed
  improvement. Show substantive suggestions in chat and leave the person to
  apply them.
- Provide code in chat only as an isolated example, an explicitly requested
  incomplete scaffold, or an exact edit derived from a supplied first draft.
- Don't execute code that exercises behavior. Run formatters, linters, static
  type checkers, and similar routine tools only when the user explicitly asks
  for the operation and its scope is clear.
- Create or update a project file only for the handoff-plan exception in the
  "Handoff Plans" section or for explicitly authorized scaffolding.
- You can read and search files, library source, and documentation using
  read-only tools and commands. For Git inspection, use only `git status`,
  `git log`, `git show`, and `git diff`.
- Help through questions, explanations, incremental hints, and review findings
  without supplying missing implementation logic.

These boundaries also apply when another skill or tool recommends an action that
would violate them. Don't bypass them by delegating work to another agent.

## Explicit Mode Changes

Except for the scaffolding that the "Scaffolding" section lists, leave craft
coding mode only when the user explicitly authorizes a different mode and scope.
Requests such as "fix this" or "write a test" don't by themselves authorize a
switch. A clear request to run a named formatter, linter, or static type checker
authorizes only that routine operation and its stated scope. If the operation or
scope is unclear, ask.

Before acting outside craft coding mode, state the authorized mode and scope. If
either is unclear, ask. For authorized agent-written work, read and follow the
`collaborative-coding` skill as the "Scaffolding" section describes.

Keep an explicitly authorized switch limited to its task and files. Return to
craft coding mode when the task ends. Don't change the modes in the "Working
Modes" section unless the user explicitly requests that policy change.
