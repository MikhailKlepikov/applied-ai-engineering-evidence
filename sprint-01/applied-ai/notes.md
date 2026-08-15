# Applied AI — Notes

## Day 1 baseline

- Date: 2026-08-13
- Duration: 118 minutes
- Mode: starting baseline, no PASS/FAIL
- Independence estimate from the learning session: approximately 40%

## Environment established

- Evidence repository cloned locally to `C:\Users\mikha\Projects\applied-ai-engineering-evidence`.
- Project `.venv` created and activated.
- The environment uses its own Python, pip and dependency directory.
- `.venv/` is ignored by Git.
- pytest 9.1.1 is available inside `.venv`.

## Mental models reproduced or corrected

- Type annotations such as `a: int` do not enforce argument types at runtime.
- `@dataclass` can generate `__init__`.
- A call to an `async def` function returns a coroutine object.
- `await` suspends the current coroutine while the awaited operation is incomplete.
- `time.sleep()` blocks the event-loop thread; absence of `await` is not itself the root cause.
- `except Exception: return None` conflates failure causes, hides traceback/observability and makes `None` ambiguous.
- A unit test isolates a service; an endpoint integration test covers the cooperation of HTTP routing, validation, DI, service logic and response mapping.

## Baseline gaps

- Typing, generics, protocols and dataclass constraints require systematic study.
- The distinction between `__new__` and `__init__` is not reproducible yet.
- Cancellation, timeouts, tasks, `TaskGroup` and event-loop scheduling are not understood deeply enough.
- Request lifecycle was described only as endpoint → service → result; routing, validation, DI, serialization and error mapping were missing.
- HTTP statuses 422, 404 and 503 were not reproduced.
- Unit and integration tests were initially not distinguishable.

## Documentation

No official documentation section was completed during the baseline. Documentation reading remains scheduled by the Sprint Contract.

## Practical work

Environment and tool checks were completed. No program implementation or debugging task was performed.

## Recall priorities

1. Coroutine object, scheduling and `await`.
2. Blocking calls inside async code.
3. Explicit error models instead of broad exception swallowing.
4. Unit versus integration test boundaries.
5. Dataclass defaults and generated methods.

## Debt

- Reproduce the environment checks with raw command output when formal evidence is required.
- Complete the scheduled Python design and async exercises.
- Record tested error scenarios once the FastAPI module exists.
