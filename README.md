# MCP Office Machine — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter IV  
**Private source:** not linked

> Docs-only public view. No internal templates, brand kits, or cluster manifests.

## Elevator

An **MCP server** that lets an agent **produce Office documents** (PPT / Word / Excel), store them in object storage, and return a **presigned URL** — chat that ships a deliverable.

## Need

| Pain | Response |
|------|----------|
| Agents that only talk | Tools for pptx / docx / xlsx generation |
| Scripts that don’t scale | One MCP surface, extend with Python modules |
| Files trapped on a pod | Upload to S3-compatible storage + signed links |
| Wire into existing agent UIs | Sit behind an MCP→HTTP bridge next to the agent platform |

## Architecture (sanitized)

```text
Agent UI ──▶ MCP gateway / bridge ──▶ MCP Office server (FastMCP)
                                            │
                                            ├─ build pptx/docx/xlsx
                                            ▼
                                         Object storage
                                            │
                                            ▼
                                      Presigned URL ──▶ user
```

**Extensibility:** new document tools = new Python modules; infra stays stable.

## What this demonstrates

- MCP / FastMCP as an integration pattern, not a demo toy
- Least-privilege cloud identity patterns for storage access
- Container-ready service for Kubernetes-style deploys

## Stack

`Python 3.12+` · `FastMCP` · `python-pptx` · `python-docx` · `openpyxl` · `boto3` · `Docker` · `Kubernetes` / EKS · S3 + presigned URLs

## Explicitly not in this repo

Server source, org templates, CI secrets, live `k8s` YAML from private clusters.


## Full source (private)

Access required. The implementation lives in a **private** repository:

- [mcp-office-machine](https://github.com/AHelijao/mcp-office-machine)

Without collaborator access, GitHub will show **404**. To request access: email [helijao.andriamandranto@gmail.com](mailto:helijao.andriamandranto@gmail.com), message on [LinkedIn](https://linkedin.com/in/helijaoa), or open an issue on **this** showcase repo — I’ll grant access case by case.

---

← back to [portfolio](https://ahelijao.github.io/) · Helijao Andriamandranto
