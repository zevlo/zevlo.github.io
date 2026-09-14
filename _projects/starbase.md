---
layout: post
title: "Starbase"
date: 2026-09-14
description: "A live dashboard for upcoming rocket launches, backed by a serverless AWS pipeline polling Launch Library 2"
github_url: "https://github.com/zevlo/starbase"
demo_url: "https://starbase.zevlo.net"
---

## About This Project

A live dashboard that counts down to the next rocket launch, flags holds,
and links to the live webcast. A serverless AWS pipeline polls Launch Library 2
every ten minutes and stores the results in DynamoDB; the whole system is
described in one Terraform stack and deploys keylessly via GitHub Actions OIDC.

Live dashboard: [starbase.zevlo.net](https://starbase.zevlo.net)
Source: [github.com/zevlo/starbase](https://github.com/zevlo/starbase)

### Technologies Used

- Python (Lambda)
- Terraform
- DynamoDB
- EventBridge, API Gateway, CloudFront, S3
- GitHub Actions (OIDC)
- pytest with moto, ruff
