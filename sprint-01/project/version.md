# Open WebUI — baseline версии

- Upstream: https://github.com/open-webui/open-webui
- Требуемый tag: `v0.11.0`
- Требуемый commit: `f9590b8017199e56d5e953657e6498e3cef1d246`
- Переключение версии в Sprint 1: запрещено без решения главного чата

## Статус дня 1

- Даты сессии: 2026-08-14 — 2026-08-15
- Длительность: 106 минут
- Режим: стартовый baseline без PASS/FAIL
- Изучен README Open WebUI `v0.11.0`
- Symbols исходного кода: не исследовались
- Изменение кода: отсутствует
- Тесты: не запускались
- Технический блокер: отсутствует

## Локальная проверка

Статус: **не проверено**.

Следующее evidence пока не собрано:

```powershell
git status --short
git branch --show-current
git rev-parse HEAD
git describe --tags --exact-match
git remote -v
```

Перед анализом исходников tag должен разрешаться в требуемый commit, а локальный `HEAD` — совпадать с ним. Несовпадение блокирует анализ до исправления состояния репозитория.

## Fork и remotes

Ожидаемая топология:

- Fork: `MikhailKlepikov/open-webui`
- `origin`: личный fork
- `upstream`: `open-webui/open-webui`

Фактические fork, clone и remotes пока не проверены.

## Результаты baseline

- Open WebUI — self-hosted AI-платформа и веб-интерфейс для работы с LLM.
- Branch — перемещающийся указатель; tag обычно обозначает фиксированный commit; полный SHA однозначно идентифицирует commit.
- Fork, clone и pull request — разные операции.
- Entry point — место, через которое управление входит в компонент.
- Read-only задача для Agent не должна создавать diff.

## Неподтверждённая архитектурная гипотеза

```text
frontend → backend → database → backend → LLM provider → backend → frontend
```

Это только гипотеза. Её нельзя считать module map или sequence diagram до подтверждения конкретными file paths, symbols, вызовами и тестами.

## Долг

- Проверить fork, `origin`, `upstream`, tag и локальный `HEAD`.
- Сформировать воспроизводимый workflow чтения крупного репозитория.
- Найти команды запуска frontend и backend.
- Найти backend/frontend entry points и конфигурацию тестов.
- Проследить один запрос по file и symbol paths.
