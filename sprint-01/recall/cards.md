# Daily Recall Registry

Карточки создаются только из реально пройденного материала и ошибок.

## Session 1

- Date: 2026-08-15
- Sprint day: 1
- Time: 23:00–23:54
- Planned: 20 minutes
- Actual: 54 minutes
- Due before session: 26
- Answered: 10
- Unchecked: 16
- PASS/FAIL: not assigned

Aggregate scores:

| Score | Count |
|---:|---:|
| 0 | 3 |
| 1 | 1 |
| 2 | 3 |
| 3 | 2 |
| 4 | 1 |
| 5 | 0 |

The session log did not preserve the exact score for each individual card. Per-card values below therefore use only supported ranges: failed cards are marked `0–2`, and successfully recalled cards are marked `3–4`.

## Registry

| ID | Source | Question/task | Last score | Next review | Interval | Status |
|---|---|---|---:|---|---|---|
| S1D1-AA-01 | Applied AI | Что изолирует `.venv`? | — | due now | 0 | unchecked |
| S1D1-AA-02 | Applied AI | Проверяет ли `a: int` тип аргумента во время выполнения? | — | due now | 0 | unchecked |
| S1D1-AA-03 | Applied AI | Что возвращает вызов функции, объявленной через `async def`? | — | due now | 0 | unchecked |
| S1D1-AA-04 | Applied AI | Что делает `await`? | 0–2 | 2026-08-16 | 1 day | failed |
| S1D1-AA-05 | Applied AI | Почему `time.sleep()` опасен внутри async-функции? | 0–2 | 2026-08-16 | 1 day | failed |
| S1D1-AA-06 | Applied AI | Почему `except Exception: return None` создаёт плохую модель ошибок? | 3–4 | 2026-08-16 | 1 day | recalled |
| S1D1-AA-07 | Applied AI | Чем unit-тест сервиса отличается от integration-теста endpoint? | — | due now | 0 | unchecked |
| S1D1-ML-01 | ML/LLM | Как вычислить евклидову норму и dot product двух векторов? | 0–2 | 2026-08-16 | 1 day | failed |
| S1D1-ML-02 | ML/LLM | Как связаны dot product, нормы и cosine similarity? | — | due now | 0 | unchecked |
| S1D1-ML-03 | ML/LLM | Что измеряет дисперсия и зачем отклонения возводятся в квадрат? | — | due now | 0 | unchecked |
| S1D1-ML-04 | ML/LLM | Чем отличаются NumPy shapes `(3,)` и `(1, 3)`? | 0–2 | 2026-08-16 | 1 day | failed |
| S1D1-ML-05 | ML/LLM | Почему shapes `(2, 3)` и `(3,)` совместимы через broadcasting? | — | due now | 0 | unchecked |
| S1D1-ML-06 | ML/LLM | Что означают TP, FP, FN, TN; как вычисляются precision и recall? | 0–2 | 2026-08-16 | 1 day | failed |
| S1D1-ML-07 | ML/LLM | Почему при высокой цене пропуска важен recall и почему повторный запуск модели не повышает его автоматически? | — | due now | 0 | unchecked |
| S1D1-DO-01 | DevOps | Чем Docker CLI отличается от Docker Engine? | 3–4 | 2026-08-16 | 1 day | recalled |
| S1D1-DO-02 | DevOps | Чем Docker image отличается от container? | — | due now | 0 | unchecked |
| S1D1-DO-03 | DevOps | Что делает `docker run --rm IMAGE`? | — | due now | 0 | unchecked |
| S1D1-DO-04 | DevOps | Почему наличие `docker.exe` не доказывает работоспособность Docker? | — | due now | 0 | unchecked |
| S1D1-DO-05 | DevOps | В каком порядке проходят DNS, TCP, TLS и HTTP? | 0–2 | 2026-08-16 | 1 day | failed |
| S1D1-OW-01 | Open WebUI | Что такое Open WebUI? | — | due now | 0 | unchecked |
| S1D1-OW-02 | Open WebUI | Чем отличаются fork, clone и pull request? | 0–2 | 2026-08-16 | 1 day | failed |
| S1D1-OW-03 | Open WebUI | Куда указывают remotes в fork-workflow? | — | due now | 0 | unchecked |
| S1D1-OW-04 | Open WebUI | Чем отличаются branch, tag и commit SHA? | 3–4 | 2026-08-16 | 1 day | recalled |
| S1D1-OW-05 | Open WebUI | Что проверить перед анализом зафиксированной версии? | — | due now | 0 | unchecked |
| S1D1-OW-06 | Open WebUI | Как искать backend entry point в незнакомом репозитории? | — | due now | 0 | unchecked |
| S1D1-OW-07 | Open WebUI | Чем должна подтверждаться sequence diagram? | — | due now | 0 | unchecked |

## Strong topics

- Consequences of broad exception swallowing.
- Basic Docker CLI versus Engine separation.
- Branch, tag and commit SHA distinction.

## Weak topics

- Vector norm and dot product.
- Classification metrics and confusion-matrix terms.
- `await` and blocking calls in async code.
- NumPy dimensionality.
- Fork workflow and pull-request direction.
- DNS → TCP → TLS → HTTP sequence.

## Corrections transferred to the learning chats

- `time.sleep()` blocks because it is synchronous and occupies the event-loop thread, not merely because `await` is absent.
- Dot product is not a vector norm; coordinate signs must be preserved.
- Precision denominator is predicted positives; recall denominator is actual positives.
- Changes are normally pushed to `origin`; a contribution PR normally targets `upstream`.
- Vector operations and network request flow were diagnosed during Day 1, not counted as fully taught topics.

Intervals for a new card: 1, 3, 7, 14 and 30 days. After an error, the interval resets to one day. Unchecked cards remain due and must not be marked learned.
