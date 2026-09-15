---
layout: post
title: "Portpeek"
date: 2026-09-14
description: "A localhost-first TCP port checker: is a service listening on this port?"
github_url: "https://github.com/zevlo/portpeek"
---

## About This Project

Portpeek tells you whether a TCP port is open, closed, or filtered. Use it for
daily questions like "did postgres come up on 5432?"

It scans 127.0.0.1 by default; scanning a remote host takes an explicit
--allow-remote and a confirmation. A --wait flag polls until every requested
port is open, so scripts can start a container and wait on it.

Source: [github.com/zevlo/portpeek](https://github.com/zevlo/portpeek)

### Technologies Used

- Rust
- tokio
- clap
- Docker
