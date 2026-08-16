# DevOps — Docker evidence

## Контекст дня 1

- Дата: 2026-08-13 — 2026-08-14
- Устройство: ноутбук Lenovo, Windows, PowerShell
- Docker Desktop: 4.40.0
- Docker CLI/Engine: 28.0.4
- Backend: WSL 2
- Обнаруженный WSL-дистрибутив: `docker-desktop`
- Пользовательский Linux-дистрибутив: не установлен

## Проверки инструментов

- Git 2.49.0
- Python 3.13.3
- pip 26.2.1
- Node.js 22.14.0
- npm 10.9.2
- curl 8.10.1
- OpenSSH 9.5p1
- VS Code 1.124.2
- Cursor 3.3.30

Глобально не найдены: `gh`, `uv`, `pytest`, `ruff`. pytest намеренно доступен внутри проектной `.venv`; глобальная установка для этого проекта не требуется.

## Проверка Docker

Выполненные команды:

```powershell
docker version
docker run --rm hello-world
docker ps
docker images hello-world
wsl --status
wsl -l -v
```

Наблюдаемые результаты:

- После запуска Docker Desktop клиент подключился к Linux Engine.
- `hello-world:latest` загружен из Docker Hub и успешно выполнен.
- Тестовый container удалён через `--rm`.
- После завершения `docker ps` не показывал запущенных containers.
- Image `hello-world:latest` остался доступен локально.

## Проверка сети

```powershell
Resolve-DnsName example.com
curl.exe -I https://example.com
```

- DNS вернул IPv4- и IPv6-адреса.
- HTTPS-запрос вернул `HTTP/1.1 200 OK`.
- `Content-Type` распознан как описание формата ответа.
- `Server: cloudflare` корректно признан недостаточным доказательством расположения origin-сервера.

## Граница evidence

Это baseline инструментов и окружения. Проектный Dockerfile не собирался; требования Sprint 1 по non-root, `.dockerignore`, healthcheck, storage и networking остаются открыты. Служебный дистрибутив `docker-desktop` не заменяет пользовательскую Ubuntu.
