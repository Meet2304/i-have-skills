---
name: docker-compose-workshop
description: Build, inspect, update, and tear down a basic WordPress and MySQL environment with Docker Compose. Use for the 14-848 Docker Compose lab or when learning the Compose lifecycle, logs, exec, image updates, and volumes.
license: GPL-3.0-only
metadata:
  category: cloud-infrastructure
  tags: docker, docker-compose, containers, wordpress, mysql
---

# Docker Compose Workshop

Use this skill for the 14-848 Docker Compose lab or a closely related learning task. For the original lab sequence, read [references/workshop.md](references/workshop.md). The supplied example is in [assets/docker-compose.yml](assets/docker-compose.yml).

## Workflow

1. Confirm Docker and Compose are available. Prefer `docker compose`; use `docker-compose` when the course environment requires Compose v1.
2. Create or inspect `docker-compose.yml`. Keep the WordPress and MySQL services, dependency, named volume, environment variables, and host port aligned.
3. Validate the file with `docker compose config` before starting services.
4. Start in detached mode, then inspect service status and WordPress logs.
5. Use `docker compose exec db bash` when the task requires inspecting the database container or its environment.
6. When changing the MySQL image tag, update the file and apply it with `docker compose up -d`; verify the recreated service.
7. Stop the environment with `docker compose down`. Treat `--volumes` as destructive and confirm before deleting named-volume data unless the user explicitly requested that deletion.

## Course fidelity

When the user asks to reproduce the course exercise exactly, follow the preserved workshop reference, including its command spelling and requested image versions. Otherwise, use current Compose syntax and explain any compatibility difference briefly.

## Safety

The example credentials are for a local learning environment only. Never reuse them for an exposed or production deployment. Do not delete volumes without explicit authorization.
