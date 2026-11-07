# Hi, I'm David

[![.NET Foundation — Member](https://img.shields.io/badge/.NET_Foundation-Member-512BD4?logo=dotnet&logoColor=white)](https://dotnetfoundation.org/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/david-stevenson-638810440)

**.NET & Distributed Systems Engineer** and **[.NET Foundation](https://dotnetfoundation.org/) Member** focused on **Clean Architecture**, **OAuth 2.1 / OIDC security**, **cloud-native orchestration (.NET Aspire & Kubernetes/Istio)**, and **automated application security**.

- Building production-style `.NET 10` systems with explicit trust boundaries, zero-signing-key resource servers, and transactional messaging sagas.
- Designing defense-in-depth CI/CD pipelines combining static analysis, SBOM supply-chain verification, live OpenAPI fuzzing, and eBPF/Falco runtime policies.
- Active member of the **[.NET Foundation](https://github.com/dotnet-foundation)** supporting open-source `.NET` ecosystem development and standards.

---

## Featured Platform — [Davids (.NET 10 Microservices & Zero-Trust BFF Reference)](https://github.com/dav-Ste/Davids)

[![Pull Request CI](https://github.com/dav-Ste/Davids/actions/workflows/pull-request-ci.yml/badge.svg?branch=main)](https://github.com/dav-Ste/Davids/actions/workflows/pull-request-ci.yml)
[![CodeQL SAST](https://github.com/dav-Ste/Davids/actions/workflows/codeql.yml/badge.svg?branch=main)](https://github.com/dav-Ste/Davids/actions/workflows/codeql.yml)
[![Staging / Nightly DAST](https://github.com/dav-Ste/Davids/actions/workflows/staging-nightly.yml/badge.svg)](https://github.com/dav-Ste/Davids/actions/workflows/staging-nightly.yml)
[![Quarterly / Release Gates](https://github.com/dav-Ste/Davids/actions/workflows/quarterly-release.yml/badge.svg)](https://github.com/dav-Ste/Davids/actions/workflows/quarterly-release.yml)
[![Production Cluster](https://github.com/dav-Ste/Davids/actions/workflows/production-cluster.yml/badge.svg?branch=main)](https://github.com/dav-Ste/Davids/actions/workflows/production-cluster.yml)

**Davids** is a multi-repository `.NET 10` e-commerce and identity platform orchestrated locally with **.NET Aspire** and hardened for **Kubernetes + Istio `STRICT` mTLS**. Customers and workforce staff are physically isolated across separate OpenIddict `RS256` OIDC realms, separate Gateway Backend-for-Frontend (BFF) cookies, and seven isolated SQL Server databases.

<p align="center">
  <a href="https://github.com/dav-Ste/Davids">
    <img src="https://raw.githubusercontent.com/dav-Ste/Davids/main/docs/architecture-and-security.svg" alt="Davids Platform Architecture & Security Topology" width="100%" />
  </a>
</p>

### Repository Map

| Domain | Repository | Highlights |
|---|---|---|
| **Orchestration & AppSec** | **[`Davids`](https://github.com/dav-Ste/Davids)** | `.NET 10` Aspire AppHost, HashiCorp Vault KV-v2 bootstrap, Grafana/Prometheus/Jaeger/Seq, K8s/Istio/Kyverno/Falco/Tetragon manifests & 5-stage security runners |
| **Platform Defaults** | **[`Davids.Shared`](https://github.com/dav-Ste/Davids.Shared)** | `Davids.ServiceDefaults` — OpenTelemetry signals, Serilog sinks, AES-GCM DataProtection key encryption, trusted forwarded headers & health checks |
| **Edge & Dual BFF** | **[`Davids.APIGateway`](https://github.com/dav-Ste/Davids.APIGateway)** | YARP `2.3` reverse proxy with dual OAuth 2.1 Authorization Code + PKCE (`S256`) BFF cookies, CSRF protection, rate limiting & zero signing keys |
| **Customer & Admin IAM** | **[`Davids.Services.Identity`](https://github.com/dav-Ste/Davids.Services.Identity)** · **[`Davids.Services.AdminIdentity`](https://github.com/dav-Ste/Davids.Services.AdminIdentity)** | Self-hosted OpenIddict `RS256` OIDC providers (`identitydb` vs. `adminidentitydb`), rotating refresh tokens with reuse detection & Redis RFC 7009 revocation |
| **Commerce & Saga** | **[`Products`](https://github.com/dav-Ste/Davids.Services.Products)** · **[`Baskets`](https://github.com/dav-Ste/Davids.Services.Baskets)** · **[`Orders`](https://github.com/dav-Ste/Davids.Services.Orders)** · **[`Payments`](https://github.com/dav-Ste/Davids.Services.Payments)** · **[`Customers`](https://github.com/dav-Ste/Davids.Services.Customers)** | Clean Architecture (`Core` / `Application` / `Infrastructure` / `Api`), EF Core SQL Server Outbox/Inbox, and asynchronous RabbitMQ checkout & payment-capture saga |
| **Web Frontends** | **[`Davids.Frontend.Web`](https://github.com/dav-Ste/Davids.Frontend.Web)** · **[`Davids.Frontend.Admin`](https://github.com/dav-Ste/Davids.Frontend.Admin)** | Customer storefront, basket, checkout & order portal (`/portal`) + Workforce RBAC (`admin` / `support` / `auditor`) catalog, stock, ledger & audit console |

---

## Other Selected Repositories

- **[`AI-Pdf-Search`](https://github.com/dav-Ste/AI-Pdf-Search)** — Document indexing and semantic search over PDFs in `C#` / `.NET`.
- **[`BookKnowledgePlatform`](https://github.com/dav-Ste/BookKnowledgePlatform)** — Structured knowledge extraction and search platform in `C#` / `.NET`.

---

## Core Stack & Focus Areas

- **Languages & Runtime:** `C# 14`, `.NET 10`, ASP.NET Core Minimal APIs, EF Core, YARP, PowerShell 7
- **Identity & Security:** OpenIddict (OAuth 2.1 / OIDC / PKCE `S256`), BFF Cookie Pattern, HashiCorp Vault, CodeQL, Semgrep, Schemathesis, Microsoft RESTler, OWASP ZAP, Syft/Grype/Trivy, Cosign
- **Data, Messaging & Mesh:** SQL Server, RabbitMQ (Transactional Outbox/Inbox), Redis, .NET Aspire, Docker, Kubernetes, Istio (`STRICT` mTLS), OpenTelemetry, Prometheus, Grafana, Jaeger, Seq
