---
title: "Grafana Alerts as Code"
excerpt: "A declarative approach to managing Grafana alerts using Jsonnet and Grizzly for version-controlled, consistent monitoring."
header:
  teaser: /assets/images/grafana-header.png
  overlay_image: /assets/images/grafana-header.png
  overlay_filter: 0.5
date: 2025-06-20
repo_url: "https://github.com/devanshu06/grafana-alerts-as-code"
blog_url: "/blog/grafana-alerts-as-code"
icons:
  - fas fa-chart-line
  - fas fa-code
tags:
  - Grafana
  - Jsonnet
  - DevOps
  - Observability
---

**Grafana • Jsonnet • Grizzly**
*Built: June 2025*

A robust framework for managing Grafana alerting rules as code, solving the "ClickOps" problem in observability pipelines.

## Key Features

*   **Declarative Definitions**: Define alerts using **Jsonnet**, a powerful data templating language, instead of manual UI entry.
*   **GitOps Workflow**: Version control your alerts, enabling code reviews, rollbacks, and history tracking.
*   **Grizzly Integration**: Uses the **Grizzly (grr)** CLI to synchronize local Jsonnet definitions with remote Grafana instances.
*   **Environment Parity**: Easily manage alerts across multiple environments (Stage, Prod) with reusable templates and parameterization.

[<i class="fab fa-github"></i> **View on GitHub**](https://github.com/devanshu06/grafana-alerts-as-code){: .btn .btn--primary}
[<i class="fas fa-blog"></i> **Read Blog Post**](/blog/grafana-alerts-as-code){: .btn .btn--light}
