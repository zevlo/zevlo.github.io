---
layout: post
title: "Mervin"
date: 2026-07-28
description: "A Unix-pipe AI CLI: pipe text in, get the model's answer back on stdout"
github_url: "https://github.com/zevlo/mervin"
---

## About This Project

Mervin puts a language model in your Unix pipes. Pipe text in; it sends that
text to a model on OpenRouter and streams the answer back to stdout. It is
quiet by default: only the model's reply is printed, so it composes with
everything else on the command line.

Four commands cover the common jobs. `diagnose` explains errors and logs, and
leads with the most likely cause. `review` critiques a diff and flags bugs and
security issues. `summarize` condenses long text. `run` takes any free-text
instruction when no specialized command fits. `usage` adds up what past calls
cost, from a log kept on your machine.

Source: [github.com/zevlo/mervin](https://github.com/zevlo/mervin)

### Technologies Used

- Rust
- tokio
- reqwest + rustls
- OpenRouter API (SSE streaming)
- Homebrew tap
