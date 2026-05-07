# Water Utility Billing — Feature & Functionality Survey

> Candidate #468 · Researched: 2026-05-07

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Springbrook (Accela) | Municipal utility billing + ERP | Commercial SaaS | https://springbrooksoftware.com |
| gWorks Utility Billing Hub | Cloud billing for local government | Commercial SaaS | https://www.gworks.com |
| WUBS | Hosted billing for rural water districts | Commercial SaaS (hosted) | https://waterdistrictbill.com |
| Muni-Link | Cloud-based utility billing for municipalities | Commercial SaaS | https://muni-link.com |
| Edmunds GovTech Utility Billing Suite | Integrated billing and collections for local government | Commercial SaaS | https://www.edmundsgovtech.com |
| AMCS Utility Billing (formerly WaterWorks) | SaaS CIS for water, sewer, electricity | Commercial SaaS (from $999/mo) | https://www.amcsgroup.com |
| PUBLIQ Software Utility Billing | Billing for municipalities and utility districts | Commercial SaaS | https://publiqsoftware.com |
| Bynry SMART360 | AI-native cloud platform for SMB utilities | Commercial SaaS | https://www.bynry.com |
| VertexOne / WaterSmart | Enterprise CIS + customer engagement for water utilities | Commercial SaaS | https://www.vertexone.ai |
| Oracle Utilities CC&B / CCS | Enterprise CIS for large utilities | Commercial (enterprise licence / SaaS) | https://www.oracle.com/utilities |

---

## Feature Analysis by Solution

### Springbrook (Accela)

**Core features**
- Meter reading management with support for all major AMI/AMR vendors
- Tiered and allocation-based rate billing including water-conservation rate structures
- Invoice generation with outsourced print-and-mail integration
- Online payment portal with real-time GL posting
- Delinquency and collections module with accounts-receivable integration
- Multi-service billing (water, sewer, stormwater on one statement)
- Budget-billing and deposit management
- Reporting for consumption, revenue, and regulatory submissions

**Differentiating features**
- Allocation Water Billing module — supports complex water-right allocation billing now available nationwide (beta tested in California)
- Real-time two-way connection between billing and online payment (no batch reconciliation)
- Part of the Accela civic-platform ecosystem enabling integration with permitting and inspections

**UX patterns**
- Module-based platform allowing utilities to select only needed components
- Web-based interface accessible from any browser
- Role-based dashboards for billing clerks, finance managers, and administrators

**Integration points**
- All major AMI/AMR meter vendors via built-in adapters
- GL and accounts-receivable modules within Springbrook suite
- IVR phone payment systems
- Outsourced bill-print and mail services
- Accela civic-platform APIs

**Known gaps**
- Per-module pricing model can make total cost opaque for smaller utilities
- Customer-facing mobile app is not a highlighted feature
- Limited AI-driven anomaly detection compared to newer platforms

**Licence / IP notes**
- Proprietary commercial software; acquired by Accela. No open-source components documented.

---

### gWorks Utility Billing Hub

**Core features**
- Centralised account management with full customer and meter history
- Custom report builder with data export capabilities
- Multi-meter vendor integration
- Billing-cycle management with batch billing runs
- Customer search and account lookup across all utility services
- Quote-based pricing with modular add-ons

**Differentiating features**
- Purpose-built for small-to-mid-sized municipalities and special districts
- Emphasis on simplicity and quick implementation (12–24 week go-live targets)
- Cloud-native with no on-premise server requirement

**UX patterns**
- Clean single-page account view with complete customer data at a glance
- Browser-based access with mobile-responsive design
- Designed for non-technical billing clerks

**Integration points**
- Multiple meter vendor data imports
- Online payment processing
- GIS service-point linkage (advertised)

**Known gaps**
- Less suited to large utilities with complex rate structures or high AMI data volumes
- Limited out-of-the-box delinquency workflow automation

**Licence / IP notes**
- Proprietary commercial SaaS. Quote-based pricing.

---

### WUBS (Water Utility Billing System)

**Core features**
- Mobile meter-reading app for field staff
- Bill generation with tiered-rate billing and interest calculation
- Payment tracking and aging reports
- Customer self-service portal for viewing bills and making payments
- Month-to-month subscription after initial 6-month period
- Data export available at any time

**Differentiating features**
- Designed exclusively for rural water districts (50–15,000 services) — not a scaled-down enterprise product
- Every feature originated from a real water district requirement
- Fully hosted — nothing to install or maintain on-site

**UX patterns**
- Deliberately simple UI matched to rural water district operational workflows
- Minimal administrative overhead

**Integration points**
- Online payment processing
- Data export in standard formats

**Known gaps**
- Limited AMI/smart-meter integration compared to enterprise solutions
- Not designed for utilities managing sewer or stormwater alongside water
- Analytics and reporting are basic compared to cloud-native peers

**Licence / IP notes**
- Proprietary commercial SaaS. Month-to-month pricing model.

---

### Muni-Link

**Core features**
- Account Central feature — complete per-customer view including address, utilities, bills, and payment history
- Billing precise to single-gallon consumption
- Penalty, interest, and lien processing
- Delinquency notices and backflow recording
- Customer portal with e-bill viewing and online payments
- Service-interruption announcements via text message, website, or social media
- Built-in CASS address certification
- Mobile apps for Android and iOS

**Differentiating features**
- Sub-meter assignment and deduction within accounts
- CASS address certification built-in (reduces returned mail)
- Multi-channel service-interruption alerts (text, web, social)
- Billing runs processable from any browser without local software

**UX patterns**
- Consistently praised for ease of use in user reviews
- Quick bill-calculation and payment-tracking workflows
- Accessible from mobile devices

**Integration points**
- Online payment gateway integration
- AMR/AMI data import
- Text and social-media notification channels

**Known gaps**
- Less feature-rich than enterprise CIS platforms for large utilities
- Advanced analytics and reporting are limited

**Licence / IP notes**
- Proprietary commercial SaaS.

---

### Edmunds GovTech Utility Billing Suite

**Core features**
- All-in-one CIS: billing, collections, and account management
- Resident Self-Service web portal with 24/7 access
- New service applications and disconnect requests online
- Online payment portal (web, IVR phone, point-of-sale)
- Integration with Finance, Service/Work Orders, Inventory Control
- Meter Management App for field staff
- Support for any utility service type (water, sewer, stormwater, electric)

**Differentiating features**
- Tightly integrated with Edmunds GovTech's broader local-government ERP (finance, payroll, HR)
- Self-service portal reduces manual data entry and call-centre load
- Work-order generation integrated with billing service events

**UX patterns**
- Designed for local government operational workflows
- Role-based views for billing clerks, supervisors, and residents
- IVR integration allows phone-based payment without staff

**Integration points**
- Edmunds GovTech Finance and ERP suite
- Work-order and inventory management modules
- IVR and point-of-sale payment hardware

**Known gaps**
- Primarily for local government context — less suitable for private water companies
- Mobile field app is meter-management focused, not a full field-service tool

**Licence / IP notes**
- Proprietary commercial SaaS targeted at local government.

---

### AMCS Utility Billing (formerly WaterWorks)

**Core features**
- Metered, stepped, and flat-rate automated billing
- Unlimited configurable rate structures and custom reports
- Customer portal for usage viewing and bill payment
- SMS payment reminders
- Streamlined meter-reading entry
- Dashboard with monthly/quarterly performance reporting
- Aged receivables, revenue, collections, and meter-reading reports
- Suitable for water, sewer, and electricity billing

**Differentiating features**
- Out-of-the-box breadth of rate structures without customisation fees
- SMS reminders reduce delinquency without requiring customer portal adoption
- Priced as an affordable mid-market SaaS (starts ~$999/mo)

**UX patterns**
- Dashboard-first design for operational visibility
- Designed for small to mid-market utilities

**Integration points**
- Meter-reading data import
- Payment gateway integration
- Report export in standard formats

**Known gaps**
- Some users find pricing high relative to comparable tools
- Limited native AMI/smart-meter head-end integration compared to enterprise platforms
- Asset management and BPM modules not included — require external integrations

**Licence / IP notes**
- Proprietary commercial SaaS. Pricing from $999/month.

---

### PUBLIQ Software Utility Billing

**Core features**
- Water, gas, and electric billing from one platform
- Complicated demand-calculation support
- Sub-meter assignment and deduction
- AMR/AMI interface for automated meter data import
- Built-in customisable reports and data exports
- Account and meter location tracking
- One-time charges alongside recurring billing

**Differentiating features**
- Handles demand calculations for commercial and industrial accounts
- Sub-meter support for complex service configurations
- Long-established presence in the municipal and utility-district market

**UX patterns**
- Designed for county, municipal, and district administrative staff
- Emphasis on accuracy and compliance for fund accounting environments

**Integration points**
- AMR/AMI technology interfaces
- Local government ERP integration
- Payment gateway

**Known gaps**
- User interface shows legacy design patterns
- Advanced customer self-service portal capabilities are limited

**Licence / IP notes**
- Proprietary commercial software. No open-source components noted.

---

### Bynry SMART360

**Core features**
- Cloud-native, AI-enabled billing platform for SMB utilities
- 25+ pre-built AMI vendor integrations (Sensus, Itron, Neptune, Badger, Landis+Gyr, Mueller, Master Meter)
- Automated meter-to-cash cycle with no manual handoffs
- AI anomaly detection flagging usage irregularities before bills are sent
- Pre-billing data validation with automated correction workflows
- Mobile meter-reading app
- Customer portal with usage history and e-billing
- GL posting and accounts-receivable sync
- Generative AI for automated regulatory report and customer-communication drafting

**Differentiating features**
- Built on modern cloud architecture — not adapted from legacy systems
- Generative AI integration for report drafting and customer communications
- Pre-built AMI head-end integrations out of the box (25+)
- Billing cycle time reduction reported (60 days → 20 days in published case study)
- AWS cloud infrastructure

**UX patterns**
- Real-time dashboards with exception-based workflows
- Designed for utility managers and billing staff at SMB utilities
- AI-flagged exceptions surfaced in dashboard for human review

**Integration points**
- AMI head-end systems (25+ pre-built)
- AWS infrastructure
- GIS systems
- Billing and ERP platforms via API

**Known gaps**
- Primarily targets SMB utilities — may lack enterprise-scale features for large municipal utilities
- Public API documentation is limited; developer resources not prominently published
- Newer entrant — smaller customer reference base than established vendors

**Licence / IP notes**
- Proprietary commercial SaaS. Pricing on request.

---

### VertexOne / WaterSmart

**Core features**
- Full CIS: meter-to-cash, work orders, customer care, billing, collections
- WaterSmart customer engagement platform with water-usage analytics
- AMI, MDM, GIS, and outage system integrations
- Multi-channel customer communications (email, voice, SMS)
- Leak and high-usage anomaly alerts with automatic customer notification
- Customer self-service portal with detailed consumption analytics
- Electronic billing presentment and payment
- Reporting for billing, field operations, and customer care

**Differentiating features**
- WaterSmart considered the gold standard for water utility customer engagement and analytics
- Combined VertexOne CIS + WaterSmart analytics covers full asset-to-cash spectrum
- Proven at scale (DC Water and Austin Water are named references)
- Group Messenger for multi-channel customer outreach campaigns

**UX patterns**
- Separate portals for utility staff and customers
- Cross-departmental insight sharing (billing, field ops, customer care)
- Analytics dashboards with consumption benchmarking and leak scoring

**Integration points**
- AMI and AMR meter systems
- MDM, GIS, and outage management systems
- Multi-channel notification (email, voice, SMS)
- CIS integration for billing sync

**Known gaps**
- Enterprise pricing and complexity — likely out of reach for small rural districts
- WaterSmart analytics was historically licensed separately before acquisition

**Licence / IP notes**
- Proprietary commercial SaaS. Enterprise pricing.

---

### Oracle Utilities CC&B / CCS

**Core features**
- Complete 360-degree customer view from meter to cash
- Support for residential, commercial, and industrial accounts
- Start/stop service workflows
- Full financial management: billing, budget plans, deposits, loans, payment processing
- Inbound and outbound customer communications management
- Support for water, electricity, gas, or blended multi-service utilities
- Oracle Customer Cloud Service (CCS): SaaS delivery with scalar and interval metering
- Regulatory compliance tools for disconnection moratoriums, medical exemptions

**Differentiating features**
- Deepest regulatory-compliance support for large utilities in multiple jurisdictions
- Handles the full complexity of large municipal or regional water authorities
- Part of Oracle's integrated energy and water software suite (MDM, GIS, field service)

**UX patterns**
- Highly configurable enterprise UI targeted at large utility back-office teams
- Role-based access with complex approval workflows

**Integration points**
- Oracle MDM, GIS, and field-service modules
- Third-party AMI head-end systems
- Enterprise ERP (Oracle Financials and third-party)
- REST APIs in CCS for integration with external systems

**Known gaps**
- Significant implementation cost and timelines (12–36 months typical)
- High total cost of ownership — not viable for small or mid-market utilities
- Complex configuration requires specialist consultants

**Licence / IP notes**
- Proprietary enterprise commercial software. Enterprise pricing only.

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Meter reading management (manual route entry, mobile app, and/or AMI/AMR import)
- Configurable rate structures (tiered, flat, budget, seasonal)
- Bill generation and delivery (print, email, portal)
- Online payment portal (credit card, ACH/eCheck, autopay)
- Delinquency management (penalty calculation, notices, disconnect scheduling)
- Customer account management (profiles, service points, deposits, history)
- Reporting and data export (revenue, aging, consumption, regulatory)
- Multi-service billing (water + sewer on one statement)

### Differentiating Features
- Real-time AMI head-end integration (25+ vendor adapters — Bynry)
- AI-driven anomaly detection before billing (Bynry)
- Allocation billing for water-right conservation programs (Springbrook)
- Gold-standard customer engagement with water-usage analytics (VertexOne/WaterSmart)
- Built-in CASS address certification (Muni-Link)
- Generative AI for regulatory reporting and customer communications (Bynry)
- Sub-meter deduction and complex demand calculations (PUBLIQ)

### Underserved Areas / Opportunities
- Open-source or freely available water utility billing — essentially none exist; the market is entirely proprietary commercial software
- Real-time AI anomaly detection is emerging but not yet standard across mid-market platforms
- Interoperability between vendor-specific AMI head-end formats lacks a universal open API standard for water utilities
- Predictive delinquency scoring — no vendor prominently offers ML-based risk scoring of accounts
- Automated regulatory submission to state agencies — most platforms stop at report generation, not e-filing
- Integrated leak-repair workflow — platforms alert customers of leaks but rarely link to a field work-order with scheduling
- Customer-facing water-budgeting and conservation tools beyond usage charts
- Multi-tenant SaaS pricing accessible to districts with fewer than 500 connections

### AI-Augmentation Candidates
- Anomaly detection on interval meter data (identify leaks, meter faults, tampering)
- Predictive delinquency scoring to prioritise collection outreach
- Automated generation of regulatory reports from billing data (generative AI)
- Natural-language query of billing and consumption data for utility managers
- Intelligent rate-structure recommendation based on consumption patterns and policy goals
- Automated customer-communication drafting for high-bill alerts, disconnect notices, and conservation tips

---

## Legal & IP Summary

All solutions surveyed are proprietary commercial software products. No open-source water utility billing or CIS platforms were identified in the research. There are no patent concerns that affect a new open-source entrant building from scratch. The AWWA, IEC, and MultiSpeak standards referenced in related research are publicly available specifications. No evidence was found of patented algorithms in any product that would constrain an independent implementation. Caution is warranted when mirroring the UX of specific tools; however, billing workflows and rate-calculation logic are standard utility-industry practice, not protectable IP.

---

## Recommended Feature Scope

**Must-have (MVP)**
- Meter reading import (manual CSV/bulk upload and at least one AMI/AMR adapter)
- Configurable tiered and flat-rate billing engine
- Account and service-point management
- Invoice generation (PDF, email delivery)
- Online payment portal (credit card and ACH/eCheck via a hosted payment page)
- Basic delinquency workflow (penalty calculation, notice generation)
- Core reports (aging, revenue summary, consumption by account)

**Should-have (v1.1)**
- Multi-service billing (water + sewer on one invoice)
- Mobile meter-reading app for field staff
- Customer self-service portal (view bills, usage history, make payments, enrol in autopay)
- Additional AMI head-end integrations (Sensus, Itron, Neptune)
- AI-based usage anomaly detection and leak alerts
- Disconnect-order scheduling with regulatory compliance rules engine

**Nice-to-have (backlog)**
- Generative AI for regulatory report drafting
- Predictive delinquency scoring
- Budget-billing and payment-plan management
- GIS service-point mapping integration
- Multi-tenant white-label mode for managed-service providers
- Green Button / ESPI-compatible data export for customer data portability
