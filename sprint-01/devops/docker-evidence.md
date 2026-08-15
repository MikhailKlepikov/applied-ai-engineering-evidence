# DevOps — Docker evidence

## Day 1 context

- Date: 2026-08-13 — 2026-08-14
- Host: Lenovo laptop, Windows, PowerShell
- Docker Desktop: 4.40.0
- Docker CLI/Engine: 28.0.4
- Backend: WSL 2
- WSL distribution observed: `docker-desktop`
- User Linux distribution: not installed

## Tool checks

- Git 2.49.0
- Python 3.13.3
- pip 26.2.1
- Node.js 22.14.0
- npm 10.9.2
- curl 8.10.1
- OpenSSH 9.5p1
- VS Code 1.124.2
- Cursor 3.3.30

Not found globally: `gh`, `uv`, `pytest`, `ruff`. pytest is intentionally available inside the project `.venv`; global installation is not required for that project.

## Docker verification

Commands run:

```powershell
docker version
docker run --rm hello-world
docker ps
docker images hello-world
wsl --status
wsl -l -v
```

Observed results:

- Docker client connected to the Linux Engine after Docker Desktop was started.
- `hello-world:latest` was pulled from Docker Hub and executed successfully.
- The test container was removed through `--rm`.
- `docker ps` showed no running containers afterward.
- The `hello-world:latest` image remained available locally.

## Network verification

```powershell
Resolve-DnsName example.com
curl.exe -I https://example.com
```

- DNS returned IPv4 and IPv6 addresses.
- HTTPS returned `HTTP/1.1 200 OK`.
- `Content-Type` was recognized as describing the response representation.
- `Server: cloudflare` was correctly treated as insufficient evidence of the origin server location.

## Evidence boundary

This was a tool and environment baseline. No project Dockerfile was built and the Sprint 1 requirements for non-root, `.dockerignore`, healthcheck, storage and networking remain open. The service distribution `docker-desktop` is not a substitute for a user Ubuntu distribution.
