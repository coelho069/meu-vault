---
title: Expose ai-memory remotely with layered access controls
tier: semantic
tags:
- ai-memory
- remote-access
- auth
- firewall
bootstrapped_at: 2026-06-20T23:11:15.316459454Z
---
# Expose ai-memory remotely with layered access controls

The `ai-memory` service moved from deployment/integration to remote exposure and then web-login repair across the latest commits.

- Commit `14886a60` deployed and integrated the MCP `ai-memory` server via Docker.
- Commit `8b7d697f` exposed `ai-memory` remotely with bearer authentication and UFW firewall.
- Commit `2dde398a` fixed web login through nginx with simple credentials.

The decision captured by these commits is that remote `ai-memory` access is not just a raw service exposure: the history explicitly mentions bearer auth, UFW, nginx, and simple credentials.

The sources do not include the credential values, whether bearer auth and nginx credentials protect the same endpoint, or the exact network topology.

### Conexões Relacionadas

- [[ai-memory-mcp-server]]
- [[MOC_Infraestrutura]]
- [[Akita_YouTube_article_processing]]
