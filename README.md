# Awesome-Financial-Services-Experience-Platform

# Top Financial Services Experience Platform Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Core Banking Engines, Digital Banking Frontends & Self-Hosted Financial CRM*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Financial Services Experience Platforms**. These tools provide the digital infrastructure for banks, credit unions, and lenders — core banking ledgers, customer-facing digital channels, loan origination, and relationship management — with a spectrum running from enterprise suites like Salesforce Financial Services Cloud and Backbase to open-source engines like Apache Fineract that power financial inclusion at population scale.

**Examples** include Apache Fineract, Mifos X, Fiducia, FinCRM, and TPT Banking (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, multi-tenant architecture, and transparent financial operations — especially relevant as **Apache Fineract** underpins financial inclusion for 400+ institutions and millions of accounts [citation:7], and **Mifos X** serves 20 million customers worldwide as a recognized Digital Public Good [citation:13].

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Salesforce Financial Services Cloud** — **The enterprise relationship management standard for financial services.** Purpose-built CRM with household relationship mapping, financial accounts, goals, and referral management. **Subscription-based** per-user. **Best for large financial institutions** already standardized on Salesforce, accepting per-seat costs and cloud dependency.

- **Adobe Financial Services Cloud** — Adobe's experience platform adapted for financial services, combining content management, analytics, and personalization for banking customer journeys.

- **Backbase** — **The digital banking engagement platform.** Omnichannel banking experiences, onboarding, and customer engagement for retail and business banking. **Enterprise licensing**. **Best for banks** wanting a polished digital frontend without building from scratch.

- **nCino** — **The cloud banking platform for loan origination and onboarding.** Built on Salesforce, with commercial loan origination, account opening, and compliance workflows. **Subscription-based**. **Best for commercial lenders** wanting loan lifecycle management on the Salesforce platform.

- **Temenos Cloud** — **The core banking standard.** Comprehensive core banking, payments, and digital banking suite for banks worldwide. **Enterprise subscription**. **Best for large banks** needing a proven, comprehensive core banking platform.

- **Fiserv DNA** — Account processing and core banking platform for banks and credit unions. **Enterprise licensing**.

- **Finastra Fusion** — Financial software suite covering core banking, payments, lending, and treasury. **Enterprise licensing**.

## Open-Source GitHub Projects

- **Apache Fineract** — **The reference open-source core banking engine.** **Apache 2.0 licensed**, an **API-first core banking platform** for loans, savings, client management, accounting, and payment processing, governed by the Apache Software Foundation [citation:7]. **Multi-tenant architecture** with isolated databases per institution, **comprehensive REST APIs** with OpenAPI documentation, configurable financial products and workflows, and integrated accounting and reporting [citation:1][citation:7]. **Proven at scale**: underpins financial inclusion for **400+ institutions and millions of accounts** [citation:7]. **Deployment**: Docker-based with PostgreSQL, running as a Spring Boot application [citation:1]. **The honest caveat**: **it is a backend engine, not a user-facing experience platform** — you need to build or integrate a frontend for customer-facing digital banking [citation:7]. **Best for microfinance institutions, credit unions, and fintechs** wanting a proven core banking foundation without proprietary licensing.

- **Mifos X** — **The full open-source core banking suite built on Fineract.** **Recognized Digital Public Good**, with **400+ institutions and 20 million customers** worldwide [citation:13]. **Includes everything Fineract provides plus reference applications**: web UI for staff, reporting plugin, **Android mobile field operations app**, and **customer mobile banking app** [citation:30]. **Multi-tenancy built in** with separate databases per institution, self-hosted so data stays with the institution [citation:13]. **The honest caveat**: **the reference apps are functional rather than polished** — institutions often customize or replace the frontend, and high-availability documentation is limited [citation:13]. **Best for organizations** wanting a complete core banking stack with mobile apps out of the box, especially in financial inclusion contexts.

- **Fiducia** — **The first open-source, multi-tenant digital banking platform for credit unions and community banks.** **MIT licensed**, built in a week with AI as an experiment, shipping **consumer banking** (accounts, loans, cards, bill pay, remote deposit), **business banking** (AI invoice processing, cash sweeps, liquidity forecasting), **FI administration** (tenant config, SSO, A/B testing, CMS), and **compliance scaffolding** mapped to SOC 2 and FFIEC controls [citation:14][citation:16]. **Open banking compliance**: Full **CFPB Section 1033** consent management with granular data scopes and one-click revocation, plus **ISO 20022 interoperability** (pain.001, pacs.008, camt.053) [citation:14]. **Core banking simulator** mocks CU*Answers, Symitar, and Fineract with chaos engineering [citation:14]. **180+ API endpoints**, three deployment modes (SaaS, dedicated, headless), and **23 adapter domains** for vendor swapping [citation:14]. **The honest caveat**: **built as a one-week experiment** — production readiness requires thorough evaluation, and it is newer than Fineract or Mifos X [citation:14]. **Best for credit unions and community banks** wanting a modern, open-source digital banking alternative to Q2 or Alkami, accepting early-stage maturity.

- **FinCRM** — **The open-source CRM and office management platform for financial services.** Available as **self-hosted open-source** with a one-time payment model (~$300 lifetime license, no per-user monthly fees) [citation:4]. **Vertical-specific architecture** with entities for **loan portfolios, compliance tracking, and complex client segmentation**, plus lead management, sales pipeline, invoicing, and client portal [citation:4]. **AI-driven insights** for predictive analytics and customer segmentation [citation:4]. **The honest caveat**: **it is a CRM, not a core banking or digital banking platform** — it manages customer relationships and office operations rather than accounts and transactions [citation:4]. **Best for mortgage lenders, insurance firms, and wealth management organizations** wanting a self-hosted financial CRM with no per-user fees.

- **TPT Banking** — **The enterprise-grade open-source banking platform.** **NestJS microservices monorepo** with **PostgreSQL, Kafka, and Casbin RBAC**, covering **retail banking, compliance (KYC/AML/SAR), open banking (PSD2/OBIE/FDX), investment banking, risk analytics, regulatory reporting (Basel III/IV), treasury, and wealth management** [citation:8]. **Money arithmetic** uses a `Money` class wrapping `decimal.js` (never JS `number`), **balance integrity** enforced by PostgreSQL triggers, **idempotency keys** on all mutating endpoints, and **step-up auth** for high-risk operations [citation:8]. **The honest caveat**: **microservices architecture requires significant infrastructure** (PostgreSQL, Redis, Kafka, Vault) and operational expertise — it is not a lightweight starter [citation:8]. **Best for fintechs and digital banks** wanting a production-grade, modular banking platform with comprehensive regulatory scaffolding.

### Additional Strong Open-Source Options

- **Frappe Lending** — **The open-source loan management system built on ERPNext.** **100% open source and API-first**, covering the entire loan lifecycle from origination to closure, with built-in compliance (DPD tracking, NPA classification), accounting, billing, taxation, and role-based access [citation:9]. **Best for lenders and NBFCs** already using or willing to adopt the Frappe/ERPNext ecosystem, wanting integrated lending and accounting.

- **Open Source Bank** — **The API-first core banking engine for fintech startups.** **Double-entry ledger** with idempotent transactions, account management, REST API with OpenAPI docs, JWT + API keys, RBAC, PII encryption, and fraud detection rules [citation:17]. **One-command Docker setup**. **Best for developers** wanting a transparent, auditable core banking foundation to build neobanks or lending platforms on.

- **FinAegis** — **The DDD/CQRS/Event Sourcing core banking prototype.** **Laravel 12 / PHP 8.4**, with **61 domain modules**, GraphQL API, Redis Streams event streaming, multi-asset accounts, and a non-custodial wallet backend . **Best for developers** wanting a reference implementation for modern event-sourced banking architecture, accepting that it is a prototype rather than a production platform.

- **Ghostfolio** — **The open-source wealth management platform.** **AGPL-3.0 licensed**, self-hosted with **multi-asset tracking** (stocks, ETFs, crypto), portfolio performance analytics, and privacy-focused data ownership [citation:29]. **Best for wealth managers and individual investors** wanting a self-hosted portfolio tracker, not a full banking platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Financial services platforms differ significantly in scope (core banking engine vs digital frontend vs CRM vs wealth management), deployment model, and regulatory readiness. **Apache Fineract and Mifos X are core banking engines** — they handle accounts, loans, and ledgers but require a separate frontend for customer experiences [citation:7][citation:13]. **Fiducia is a digital banking frontend** built as a one-week experiment — evaluate production readiness carefully [citation:14]. **FinCRM is a financial services CRM**, not a banking platform [citation:4]. **TPT Banking is a comprehensive microservices platform** requiring significant infrastructure [citation:8]. **Core banking platforms must comply with financial regulations** (Basel III/IV, PSD2, CFPB Section 1033) and undergo security audits before handling real funds.
- Self-hosted open-source solutions require proper security hardening, database configuration (PostgreSQL for Fineract and TPT Banking), high-availability design, and regulatory compliance verification before production deployment.

---

**Made for financial institution technology teams, fintech developers, and organizations choosing financial services platforms that match their regulatory needs and self-hosting capabilities.**
Let's make financial services experience platforms more open, multi-tenant, and developer-friendly.
