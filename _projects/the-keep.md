---
title: "The-Keep"
excerpt: "An Ansible-driven orchestration solution for provisioning, hardening, and operating a production-grade HashiCorp Vault cluster in HA mode."
header:
  teaser: /assets/images/vault-header.png
  overlay_image: /assets/images/vault-header.png
  overlay_filter: 0.5
date: 2025-12-25
repo_url: "https://github.com/devanshu06/the-keep"
icons:
  - fas fa-shield-alt
tags:
  - Ansible
  - HashiCorp Vault
  - Security
---

**Ansible • HashiCorp Vault • Automation • Security**  
*Built: Dec - 2025*

An Ansible-driven orchestration solution for provisioning, hardening, and operating a production-grade [**HashiCorp Vault**](https://developer.hashicorp.com/vault) cluster in High Availability (HA) mode.

## Key Features

*   **Automated HA Deployment**: Provisions a three-node Vault cluster using Raft storage, eliminating the need for external storage backends like Consul.
*   **Infrastructure as Code**: Fully customizable configuration via Ansible group variables, supporting both **AWS** and **Google Cloud Platform (GCP)**.
*   **Production Hardening**: Includes automated TLS certificate management, OS-level hardening, and disaster recovery workflows (Snapshot/Restore).
*   **Operational Excellence**: Built-in support for Google SSO (OIDC) integration and standardized unseal processes.

[<i class="fab fa-github"></i> **View on GitHub**](https://github.com/devanshu06/the-keep){: .btn .btn--primary}
