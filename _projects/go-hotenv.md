---
title: "Go-HotEnv"
excerpt: "A robust solution for enabling hot-reloadable environment variables in Go applications running on Kubernetes."
header:
  teaser: /assets/images/go-header.png
  overlay_image: /assets/images/go-header.png
  overlay_filter: 0.5
date: 2025-10-06
repo_url: "https://github.com/devanshu06/go-hotenv"
blog_url: "/blog/go-hotenv"
icons:
  - fab fa-golang
tags:
  - Golang
  - Kubernetes
  - DevEx
---

**Golang • Kubernetes • Developer Experience**  
*Built: Oct 2025*

A robust solution for enabling hot-reloadable environment variables in Go applications running on Kubernetes, eliminating the need for pod restarts during configuration changes.

## Key Features

*   **Real-time Watching**: Utilizes `fsnotify` to detect atomic `ConfigMap` updates (symlink swaps) on mounted volumes.
*   **Thread-Safe Concurrency**: Implements `sync.RWMutex` to safely swap configuration structs at runtime without race conditions.
*   **Zero Downtime**: Decouples deployment lifecycles from configuration lifecycles, significantly reducing the inner development loop.

[<i class="fab fa-github"></i> **View on GitHub**](https://github.com/devanshu06/go-hotenv){: .btn .btn--primary} 
[<i class="fas fa-blog"></i> **Read Blog Post**](/blog/go-hotenv){: .btn .btn--light}
