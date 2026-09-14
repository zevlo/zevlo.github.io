---
layout: post
title: "Starbase"
date: 2026-03-20
description: "A live dashboard for upcoming rocket launches, backed by a serverless AWS pipeline polling Launch Library 2"
github_url: "https://github.com/zevlo/starbase"
demo_url: "https://starbase.zevlo.net"
---

## About This Project

Starbase is a live dashboard for upcoming rocket launches. It shows a countdown
to the next launch, tells you when a launch is on hold and why, and links to
the live video when one exists. A small JSON API serves the same data for
anyone who wants to build on it.

Behind the page, a serverless pipeline on AWS keeps the data fresh. Every ten
minutes, a scheduled Lambda function asks Launch Library 2 for the next 20
launches and saves them to DynamoDB. CloudFront serves the dashboard and caches
API reads for 30 seconds at the edge. A counter in DynamoDB caps upstream
requests at 12 per hour, under the data source's free limit of 15. The whole
system lives in one Terraform stack and deploys through GitHub Actions with no
stored cloud credentials.

Source: [github.com/zevlo/starbase](https://github.com/zevlo/starbase)
Dashboard: [starbase.zevlo.net](https://starbase.zevlo.net)

### Technologies Used

- Python (Lambda)
- Terraform
- DynamoDB
- EventBridge, API Gateway, CloudFront, S3
- GitHub Actions (OIDC)
- pytest with moto, ruff
