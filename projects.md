---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
---

A selection of systems, platforms, and tooling I’ve worked on or built.

## <i class="fas fa-shield-alt"></i> The Keep
**Ansible • HashiCorp Vault • Automation • Security**

**[<i class="fab fa-github"></i> View on GitHub](https://github.com/devanshu06/the-keep)**

An Ansible-driven orchestration solution for provisioning, hardening, and operating a production-grade [**HashiCorp Vault**](https://developer.hashicorp.com/vault) cluster in High Availability (HA) mode.

*   **Automated HA Deployment**: Provisions a three-node Vault cluster using Raft storage, eliminating the need for external storage backends like Consul.
*   **Infrastructure as Code**: Fully customizable configuration via Ansible group variables, supporting both **AWS** and **Google Cloud Platform (GCP)**.
*   **Production Hardening**: Includes automated TLS certificate management, OS-level hardening, and disaster recovery workflows (Snapshot/Restore).
*   **Operational Excellence**: Built-in support for Google SSO (OIDC) integration and standardized unseal processes.

---

> I value **systems that explain themselves when they fail**.