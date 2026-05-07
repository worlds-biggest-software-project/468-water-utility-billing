# Water Utility Billing

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An open-source, AI-native billing platform that automates the meter-to-cash cycle for water utilities of every size.

Water Utility Billing is a complete billing and customer information system for water utilities -- from small rural water districts to mid-sized municipalities. It handles meter reading ingestion, tiered rate calculation, invoice generation, payment processing, and delinquency management in a single platform, replacing the patchwork of paper routes, spreadsheets, and legacy COBOL systems that many utilities still depend on.

---

## Why Water Utility Billing?

- **No open-source alternative exists.** Every water utility billing product on the market is proprietary commercial software. Rural districts and small municipalities have no budget-friendly, community-driven option and are locked into vendor pricing with limited negotiating power.
- **Legacy systems drive high operational costs.** Many utilities still rely on manual meter-reading routes, hand-calculated bills, and mailed statements, leading to billing errors, delayed revenue, and unnecessary labour costs.
- **Incumbent pricing excludes small utilities.** Enterprise CIS platforms like Oracle CC&B require 12-36 month implementations and enterprise-level budgets. Even mid-market SaaS products start at ~$999/month, which is prohibitive for districts with fewer than 500 connections.
- **AMI interoperability is fragmented.** Each AMI vendor uses proprietary data formats with no universal open API standard for water meter data, forcing utilities to pay for vendor-specific integrations.
- **AI capabilities are emerging but not standard.** Only one surveyed vendor (Bynry) offers AI-driven anomaly detection and generative AI for reporting. The rest of the market has not yet adopted these capabilities, leaving an opportunity for an AI-native platform built from the ground up.

---

## Key Features

### Meter Reading & Data Ingestion

- Mobile meter-reading app for field staff with route sequencing and exception flagging
- AMI/AMR integration for automated ingestion of smart meter reads via API or file import
- Meter data validation with estimated reads, rejected reads, and auditable override history
- Support for multiple AMI head-end vendors (Sensus, Itron, Neptune, Badger, Landis+Gyr, Mueller, Master Meter)

### Billing & Rate Engine

- Configurable tiered, flat-rate, inclining-block, seasonal, and budget-billing rate structures
- Multi-service billing -- water, sewer, and stormwater on a single invoice
- Base charges, consumption charges, taxes, and sewer add-ons calculated automatically per account class
- Sub-meter assignment and deduction for complex service configurations

### Customer & Account Management

- Customer profiles with service-point linkage, deposits, ownership transfers, and correspondence history
- Customer self-service portal for viewing bills, usage history, making payments, and enrolling in autopay
- Online payment via credit card, ACH, and e-check through a hosted payment page (PCI-DSS compliant)
- Electronic bill presentment and delivery via email, SMS, and portal

### Delinquency & Collections

- Automated penalty calculation on overdue balances
- Delinquency notice generation with configurable notice periods
- Disconnect-order scheduling with regulatory compliance rules (medical-hardship exemptions, seasonal moratoriums)
- Reconnect fee processing and lien management

### Reporting & Integration

- Core reports: aged receivables, revenue summaries, consumption by account, and regulatory submissions
- GL posting of billing transactions and accounts-receivable sync
- GIS linkage for service-point mapping and work-order generation
- Data export in standard formats for auditing and regulatory compliance

---

## AI-Native Advantage

Water Utility Billing is designed from the ground up to leverage AI where incumbents cannot. Usage-anomaly detection analyses interval meter data to identify leaks, meter faults, and potential tampering before bills are sent -- automatically notifying customers of suspected issues. Predictive delinquency scoring prioritises collection outreach by identifying at-risk accounts before balances become unrecoverable. Generative AI drafts regulatory reports from billing data and produces customer communications for high-bill alerts, disconnect notices, and conservation tips, reducing administrative burden across the organisation.

---

## Tech Stack & Deployment

The platform targets self-hosted and cloud deployment models, making it accessible to utilities with varying IT capabilities. The billing engine supports configurable rate structures without code changes via a rules engine or rate-builder UI. AMI integration uses adapter-based architecture to support multiple meter vendor formats. Payment processing relies on tokenisation and hosted payment pages to minimise PCI-DSS compliance scope. Time-series data strategies address the high-volume interval data generated by smart meters (reads as frequent as every 15 minutes across thousands of meters).

---

## Market Context

The water utility billing software market in 2026 includes more than 50 products listed on Capterra and GetApp, ranging from hosted solutions for rural co-ops to enterprise CIS platforms for large municipal authorities. Pricing spans from month-to-month subscriptions (WUBS for rural districts) through mid-market SaaS at ~$999/month (AMCS) to enterprise-only contracts (Oracle, VertexOne). Primary buyers are municipal water departments, rural water districts, and regional water authorities seeking to modernise aging billing infrastructure.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
