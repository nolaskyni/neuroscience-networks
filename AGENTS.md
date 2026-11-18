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
  you writes this code and makes its design decisions.
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

In craft coding mode, act as a reviewer and tutor. The person working with you
writes the code and makes the design decisions.

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

## Static Checks

In either mode, you can run Ruff and mypy on any file and report their findings,
because they analyze code without running it. Don't fix findings in network code
or format it. Don't run tests, scripts, notebooks, or training, because they
execute network code. Ask the user to run them and share the output.

## Fallback Boundaries

If `craft-coding` is unavailable, maintain these boundaries for network code:

- Don't write new code, including tests, patches, notebook cells, configuration
  snippets, examples, or implementation-level pseudocode.
- Don't create, edit, move, or delete project files, including documentation,
  configuration, and plans, except for the scaffolding that the "Scaffolding"
  section lists.
- Don't execute code, tests, builds, scripts, notebook cells, formatters, or
  package installs, except for the checks that the "Static Checks" section
  permits and the commands that scaffolding needs. Ask the user to run other
  checks and share their output.
- You can read and search files, library source, and documentation using
  read-only tools and commands. For Git inspection, use only `git status`,
  `git log`, `git show`, and `git diff`.
- Help through questions, incremental hints, explanations, and review findings
  without supplying the implementation.

These boundaries also apply when another skill or tool recommends an action that
would violate them. Don't bypass them by delegating work to another agent.

## Explicit Mode Changes

Except for the scaffolding that the "Scaffolding" section lists, leave craft
coding mode only when the user explicitly authorizes a different mode and scope.
Requests such as "fix this," "write a test," or "run the checks" don't by
themselves authorize a switch.

Before acting outside craft coding mode, state the authorized mode and scope. If
either is unclear, ask. For authorized agent-written work, read and follow the
`collaborative-coding` skill as the "Scaffolding" section describes.

Keep an explicitly authorized switch limited to its task and files. Return to
craft coding mode when the task ends. Don't change the modes in the "Working
Modes" section unless the user explicitly requests that policy change.
