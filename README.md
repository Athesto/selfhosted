# 📦 selfhosted

> My self-hosted infrastructure, powered by Docker Compose.



## 📖 About

This repository contains the deployment and configuration of the self-hosted services running on my personal infrastructure.

It is designed to be a single source of truth for installing, maintaining, and rebuilding every service with as little guesswork as possible.

The applications themselves are **not developed here**. This repository focuses on how they are deployed, configured, connected, and maintained.



## 🎯 Philosophy

A good infrastructure should be reproducible.

If I ever need to migrate to another machine or rebuild everything from scratch, this repository should contain every decision required to do so.

Documentation should outlive memory.



## 📂 Project Layout

```text
.
├── bookmarks/
├── services/
├── volumes/
├── LICENSE
└── README.md
```

### 🔖 bookmarks

Quick links to the services I use most often.

This directory can contain symbolic links to services under `services/`.

Example:

```text

bookmarks/
├── jellyfin -> ../services/jellyfin
└── file-browser -> ../services/file-browser

```

### 📦 services

Each service lives in its own directory.

Every service is completely independent and contains its own:

- `docker-compose.yml`
- `.env.example`
- service-specific configuration


### 💾 volumes

Persistent application data.

This directory is intentionally excluded from version control and should always be included in backups.



## ⚙️ Principles

- One service, one Compose project.
- Services should be independent.
- Configuration and data are separated.
- Infrastructure should be reproducible.
- Prefer simplicity over cleverness.
- Everything should be documented.



## 🚀 Adding a new service

1. Create a new directory under `services/`.
2. Add a `docker-compose.yml`.
3. Create an `.env.example` if needed.
4. Mount persistent data under `volumes/`.
5. Connect to the shared network when required.
6. Document anything that isn't obvious.



## 📝 Notes

This repository evolves over time.

Whenever a deployment becomes easier, clearer, or more maintainable, the repository should evolve as well.
