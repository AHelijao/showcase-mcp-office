# MCP Office Machine — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter IV

> Sanitized public view. No internal branding, templates, or deployment manifests from private systems.

## What it is

An **MCP (Model Context Protocol) server** that turns an agent chat into deliverables: generate **PowerPoint / Word / Excel**, store artifacts, return **signed download URLs**. Containerized and deployable next to an agent platform.

## Problem

Chat-only agents talk; operators still need documents. One-off scripts don’t scale. You want reusable tools the model can call, with access control and cloud storage — not paste-into-slides.

## What this shows

- FastMCP tool surface for document generation
- Agent → tool → object storage → presigned URL path
- Container + orchestration mindset (Docker / Kubernetes)

## Stack

`Python` · `FastMCP` · `python-pptx` / docx / xlsx · `Docker` · `Kubernetes` · `S3` (+ IRSA-style cloud identity patterns)

## What’s intentionally omitted

Internal document templates, org-specific styling, CI secrets, and live cluster configs.

## Status

Capability showcase. Full server code stays private.

---

*Helijao Andriamandranto — software & cybersecurity*
