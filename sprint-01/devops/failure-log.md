# DevOps — Failure log

Для каждого сбоя фиксируется полный диагностический цикл.

| Дата | Сбой | Симптом | Гипотеза | Проверка | Причина | Исправление | Проверка исправления | Evidence |
|---|---|---|---|---|---|---|---|---|
| 2026-08-13 | Docker CLI не соединяется с Engine | CLI установлен, но раздел `Server` недоступен; канал `dockerDesktopLinuxEngine` отсутствует; `docker-desktop` имеет статус `Stopped` | Docker Desktop и Engine не запущены | `docker version`, `wsl -l -v` и проверка состояния Docker Desktop | Docker Engine не работал | Запущен Docker Desktop | В `docker version` появился раздел `Server`; `docker-desktop` перешёл в `Running`; `docker run --rm hello-world` завершился успешно | [Docker evidence](docker-evidence.md) |

## Ограничение зачёта

Этот сбой возник естественно во время baseline и полезен как диагностическое evidence. Он **не заменяет** три обязательных намеренно созданных сбоя Sprint 1:

1. неверный port binding;
2. ошибка permissions/пользователя;
3. проблема network/DNS/volume.
