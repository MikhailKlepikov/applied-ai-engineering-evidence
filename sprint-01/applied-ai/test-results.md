# Applied AI — Test results

## Day 1 environment checks

- Date: 2026-08-13
- Repository state: local evidence repository
- Python: 3.13.3
- Git: 2.49.0.windows.1
- Global pip: 26.2.1
- `.venv` pip: 25.0.1
- `.venv` pytest: 9.1.1

## Commands represented by the session

```powershell
python --version
git --version
pip --version
.\.venv\Scripts\python.exe -m pip --version
.\.venv\Scripts\python.exe -m pytest --version
git status --short
```

## Observed result

```text
Python 3.13.3
Git 2.49.0.windows.1
global pip 26.2.1
.venv pip 25.0.1
pytest 9.1.1
git status --short: empty
```

The values above were recorded from the learning session. Raw terminal output was not committed, so these checks must be rerun before they are used as formal acceptance evidence.

## Program tests

No application tests were run on Day 1. The pytest invocation only verified that the test runner is installed inside the virtual environment.

## Checked error scenarios

| Scenario | Expected | Actually observed | Status |
|---|---|---|---|
| Global Python cannot initially import pytest | Project dependencies should live in `.venv` | pytest became available after using the project environment | Environment check only |
| `.venv/` appears in Git changes | Virtual environment must not be committed | `git status --short` was empty | Verified in session |
