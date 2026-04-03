# CLAUDE.md — AI Assistant Guide for `freenergy`

This file provides context, conventions, and workflow guidance for AI coding
assistants (Claude Code and similar tools) working in this repository.

> **Status**: This repository is newly initialized. Update this file as the
> project grows to keep the guidance accurate and complete.

---

## Repository Overview

| Field       | Value                                     |
|-------------|-------------------------------------------|
| Name        | `freenergy`                               |
| Remote      | `Yougourta/freenergy`                     |
| Primary branch | `main` (to be confirmed once established) |

The purpose and technology stack of this project are not yet established.
Expand this section once the project has been bootstrapped.

---

## Branch Conventions

- All work happens on feature branches, never directly on `main`/`master`.
- Branch naming pattern used by AI agents: `claude/<short-description>-<id>`
  - Example: `claude/add-claude-documentation-LXV5o`
- Always push with `-u` to set the upstream:
  ```bash
  git push -u origin <branch-name>
  ```
- Do **not** force-push to shared or protected branches without explicit permission.

---

## Git Commit Style

- Use short, imperative commit messages (≤ 72 chars for the subject line).
- Format:
  ```
  <verb> <what was changed>

  Optional longer explanation if needed.
  ```
- Good examples:
  - `Add initial project scaffold`
  - `Fix null pointer in energy calculator`
  - `Refactor data pipeline for readability`
- Avoid vague messages like `fix stuff` or `update`.

---

## Development Workflow

> Fill in this section once the project has a defined tech stack and tooling.

Typical flow (to be updated):

1. Create a feature branch from `main`.
2. Make changes; run tests locally before committing.
3. Commit with a clear message.
4. Push the branch and open a PR targeting `main`.
5. Address review comments, then merge.

---

## Project Structure

> This section will be populated once the codebase is established. Common
> top-level directories to document here:
>
> - `src/` — main application source
> - `tests/` — test suite
> - `docs/` — project documentation
> - `scripts/` — utility/build scripts
> - Configuration files (`.env.example`, linter configs, etc.)

---

## Testing

> Document the test runner, how to run tests, and coverage expectations once
> they are set up.

```bash
# Example — update when the project is bootstrapped
npm test        # or: pytest / cargo test / go test ./...
```

- Always run the full test suite before pushing.
- New features should include corresponding tests.
- Do not delete or skip tests without a documented reason.

---

## Code Conventions

> Update with language- and framework-specific rules once the stack is known.

General principles that apply regardless of stack:

- Prefer clarity over cleverness.
- Keep functions small and focused on a single responsibility.
- Name variables and functions descriptively.
- Do not commit secrets, credentials, or `.env` files — use `.env.example`
  with placeholder values instead.
- Remove dead code rather than commenting it out.

---

## Environment Variables

- Copy `.env.example` to `.env` for local development (never commit `.env`).
- Document every required variable in `.env.example` with a comment explaining
  its purpose.
- Example format:
  ```
  # Base URL for the API server
  API_URL=https://api.example.com
  ```

---

## AI Assistant Guidelines

When working in this repository, AI assistants should:

1. **Read before editing** — always read a file before modifying it.
2. **Stay on the designated branch** — check `git branch` and work on the
   branch specified in the task (e.g., `claude/<description>-<id>`).
3. **Minimal scope** — only change what was asked; do not refactor surrounding
   code or add unrequested features.
4. **No destructive git ops** without explicit user confirmation:
   - `git reset --hard`, `git push --force`, `git clean -f`, branch deletion.
5. **Commit atomically** — one logical change per commit.
6. **Update this file** when adding significant new patterns, tooling, or
   conventions so it stays accurate for future sessions.
7. **Do not create PRs** unless the user explicitly requests one.
8. **Do not guess URLs** — only use URLs provided by the user or found in the
   codebase.

---

## Security

- Never introduce command injection, SQL injection, XSS, or other OWASP Top 10
  vulnerabilities.
- Validate all input at system boundaries (user input, external APIs).
- Do not hardcode credentials or tokens in source files.

---

*Last updated: 2026-04-03 — repository is newly initialized with no source code yet.*
