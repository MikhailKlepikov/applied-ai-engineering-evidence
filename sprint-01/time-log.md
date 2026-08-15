# Time log

Время одной работы учитывается только один раз. Перерывы не учитываются.

| Фактическая дата | День | Блок | Направление | План, мин | Факт, мин | Результат | Evidence/ссылка | Долг |
|---|---:|---|---|---:|---:|---|---|---|
| 2026-08-13 | 1 | A | Applied AI | 110 | 118 | Стартовый baseline; проверены Python, Git, pip, изолированная `.venv` и pytest | [notes](applied-ai/notes.md), [checks](applied-ai/test-results.md) | Закрепить typing, dataclasses, ошибки, asyncio, HTTP lifecycle и тестирование |
| 2026-08-13 | 1 | B1 | ML/LLM | 55 | 66 | Ручной baseline по математике, shapes, broadcasting и метрикам | [metrics](ml-llm/metrics.md) | Нормы, dot product, cosine similarity, NumPy shapes, autograd и ML workflow |
| 2026-08-13 — 2026-08-14 | 1 | B2 | DevOps | 55 | 73 | Проверены инструменты, Docker Engine, DNS и HTTPS; диагностирован остановленный Engine | [Docker evidence](devops/docker-evidence.md), [failure log](devops/failure-log.md) | Linux, network flow, Git remotes и намеренные инфраструктурные сбои |
| 2026-08-14 — 2026-08-15 | 1 | C | Project / Open WebUI | 60 | 106 | Стартовый baseline без изменения кода; изучен README; сформирована неподтверждённая гипотеза request flow | [version baseline](project/version.md) | Проверить fork/remotes/HEAD и научиться находить entry points и тесты |
| 2026-08-15 | 1 | Recall | Daily Recall | 20 | 54 | Проверено 10 из 26 новых карточек; выявлены 7 слабых карточек | [registry](recall/cards.md) | Повторить 10 карточек 2026-08-16; 16 карточек ещё не проверены |
| **Итого** | **1** |  |  | **300** | **417** | **Baseline и организация завершены без PASS/FAIL** |  | **Перерасход: 117 минут** |

## Отклонение расписания

Sprint Day 1 фактически занял период 2026-08-13 — 2026-08-15. Это зафиксировано как один учебный день; календарь контракта автоматически не перенумеровывался. Причины перерасхода: расширенный baseline и разбор ошибок. Следующие сессии должны укладываться в заявленные timebox.
