---
title: AI-memory MCP server deployment
tier: semantic
tags:
- ai-memory
- mcp
- docker
- nginx
- auth
bootstrapped_at: 2026-06-20T23:11:15.316459454Z
---
# AI-memory MCP server deployment

The latest supplied commits describe deployment and remote exposure of an `ai-memory` MCP server.

Timeline from the log:

- Commit `14886a60` added deployment and integration of the `ai-memory` MCP server via Docker, with “akitaonrails” mentioned in the commit subject.
- Commit `8b7d697f` exposed `ai-memory` remotely using bearer authentication and a UFW firewall.
- Commit `2dde398a` fixed web login for `ai-memory` via nginx using simple credentials.

The log indicates the deployment stack includes Docker, nginx, bearer auth, and UFW. It does not provide compose files, ports, credential names, firewall rules, or nginx locations, so those must be read from the repository or host configuration.

### Conexões Relacionadas

- [[0003-expose-ai-memory-remotely-with-layered-access-controls]]
- [[Akita_YouTube_article_processing]]
- [[0001-guard-startup-with-venv-and-single-instance-protection]]
