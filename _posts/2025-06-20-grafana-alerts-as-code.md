---
layout: single
title: "How to Manage Grafana Alerts as Code using Jsonnet & Grizzly"
date: 2025-06-20
permalink: /blog/grafana-alerts-as-code
excerpt: "The story of moving from manual 'ClickOps' to a robust, version-controlled alerting pipeline using Grizzly and Jsonnet."
categories:
  - DevOps
  - Observability
tags:
  - grafana
  - jsonnet
  - grizzly
  - infrastructure-as-code
search: true
classes: wide
header:
  teaser: /assets/images/grafana-header.png
  overlay_image: /assets/images/grafana-header.png
  overlay_filter: 0.5
toc: true
---

It started with a missing alert.

We’ve all been there. A critical service hiccups, latency spikes, and... silence. No pager duty alarm, no Slack notification. You only find out when a user complains. You scramble to check Grafana, only to realize that the alert you *swore* you configured in Production was actually only set up in Staging.

This was the moment I realized that "ClickOps"—managing critical infrastructure by clicking through a GUI—was a ticking time bomb. While Grafana’s UI is fantastic for visualization, manually managing complex alerting rules across multiple environments is a recipe for drift, inconsistency, and sleepless nights.

### The Problem: Drift and Doubt

As our infrastructure grew, the cracks in the manual approach began to show:
*   **No Source of Truth**: "Who changed the CPU threshold to 95%?" There was no Git history to tell us.
*   **Inconsistency**: Production alerts slowly drifted away from Staging configurations as hotfixes were applied manually and forgotten.
*   **Toil**: Recreating a suite of alerts for a new microservice meant hours of tedious, error-prone copy-pasting.

I wanted my alerts to be treated with the same rigor as my application code: **versioned, reviewed, and automated.**

### The Solution: Grizzly + Jsonnet

I set out to build a solution that would allow us to define alerts as code. That's when I found **Grizzly** and **Jsonnet**.

*   **Jsonnet** is our data modeling language. It allows us to define alerts as templates. It’s not just static YAML; it’s code. We can create functions, variables, and imports to keep our alert definitions DRY (Don't Repeat Yourself).
*   **Grizzly (grr)** is the engine. It takes that Jsonnet code and talks to the Grafana API. It acts like `kubectl apply`, but for your monitoring stack.

### How It Works

Instead of clicking "New Alert" in the browser, I now define a rule in my IDE:

```jsonnet
local alert = import 'templates/alert-rule-template.jsonnet';

alert.new(
  name='High API Latency',
  query='avg(http_request_duration_seconds) > 1.5',
  severity='critical',
  env='production'
)
```

With a simple `grr apply`, this rule is pushed to Grafana. If I want to verify the state, `grr diff` shows me exactly what will change before I apply it.

### The Result

Moving to **Grafana Alerts as Code** has completely changed our workflow.
1.  **Confidence**: I know exactly what is deployed where. The code *is* the documentation.
2.  **Speed**: Spinning up a new environment with a full suite of alerts takes seconds.
3.  **Sanity**: No more pagers calls due to configuration drift or "fat-finger" errors in the UI.

If you are tired of wrestling with UI-managed alerts, I've open-sourced the pattern and templates I use. Check out the repository below to see how you can start building your own alerting-as-code pipeline.

---

[<i class="fab fa-github"></i> **View the Code**](https://github.com/devanshu06/grafana-alerts-as-code){: .btn .btn--primary}
[<i class="fas fa-project-diagram"></i> **View Project Details**](/projects/grafana-alerts-as-code/){: .btn .btn--info}

