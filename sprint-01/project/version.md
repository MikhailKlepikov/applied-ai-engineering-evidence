# Open WebUI — Version baseline

- Upstream: https://github.com/open-webui/open-webui
- Required tag: `v0.11.0`
- Required commit: `f9590b8017199e56d5e953657e6498e3cef1d246`
- Version switching in Sprint 1: prohibited without a decision from the main chat

## Day 1 status

- Session dates: 2026-08-14 — 2026-08-15
- Duration: 106 minutes
- Mode: starting baseline without PASS/FAIL
- README inspected: Open WebUI `v0.11.0`
- Source symbols inspected: none
- Code changes: none
- Tests: none
- Technical blocker: none

## Local verification

Status: **not verified**.

The following evidence has not yet been collected:

```powershell
git status --short
git branch --show-current
git rev-parse HEAD
git describe --tags --exact-match
git remote -v
```

Before source analysis, the tag must resolve to the required commit and local `HEAD` must match it. A mismatch blocks analysis until the repository state is corrected.

## Fork and remotes

Expected topology:

- Fork: `MikhailKlepikov/open-webui`
- `origin`: personal fork
- `upstream`: `open-webui/open-webui`

Actual fork, clone and remotes have not been verified.

## Baseline findings

- Open WebUI is a self-hosted AI platform and web interface for working with LLMs.
- A branch is a moving reference, a tag normally names a fixed commit, and a full SHA identifies one commit.
- Fork, clone and pull request are different operations.
- An entry point is the place where control enters a component.
- A read-only Agent task must not create a diff.

## Unverified architecture hypothesis

```text
frontend → backend → database → backend → LLM provider → backend → frontend
```

This is only a hypothesis. It must not be used as a module map or sequence diagram until confirmed by concrete file paths, symbols, calls and tests.

## Debt

- Verify fork, `origin`, `upstream`, tag and local `HEAD`.
- Establish a reproducible large-repository reading workflow.
- Find commands for starting frontend and backend.
- Find backend/frontend entry points and test configuration.
- Trace one request using file and symbol paths.
