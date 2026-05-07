# Standards & API Reference

> Project: Water Utility Billing · Generated: 2026-05-07

---

## Industry Standards & Specifications

### AWWA Standards (American Water Works Association)

AWWA Standards are consensus documents accredited by ANSI. More than 200 standards cover all areas of water treatment, distribution, metering, and utility management.

| Standard | Title | Relevance |
|----------|-------|-----------|
| ANSI/AWWA C700 | Cold-Water Meters – Displacement Type, Metal Alloy Main Case | Specifies accuracy and construction requirements for the most common residential water meters used in utility billing. |
| ANSI/AWWA C701 | Cold-Water Meters – Turbine Type | Accuracy and testing standards for turbine-type meters used in commercial and industrial accounts. |
| ANSI/AWWA C708 | Cold-Water Meters – Multijet Type | Standards for small-bore multijet meters (5/8 in.–2 in.) commonly used in residential service. |
| ANSI/AWWA C715 | Remote-Transmission Water Meters (Smart Meters) | Specifies requirements for smart meters and remote-read devices; foundational for AMI/AMR integration in billing systems. |
| AWWA M1 | Principles of Water Rates, Fees, and Charges (6th ed.) | The definitive manual for designing tiered, inclining-block, seasonal, and budget-billing rate structures. |
| AWWA M5 | Water Utility Management (3rd ed.) | Covers utility financial management, billing practices, and performance benchmarking. |
| AWWA G400 | Utility Management System | Describes utility management system requirements including billing, customer service, and data management. |
| AWWA M22 | Sizing Water Service Lines and Meters | Guides meter sizing decisions affecting billing accuracy and customer account classification. |

AWWA Standards List: https://www.awwa.org/standards/standards-list/
AWWA Metering and Accountability policy: https://www.awwa.org/policy-statement/metering-and-accountability/

---

### IEC Standards (International Electrotechnical Commission)

Although originating in the electrical sector, IEC 61968 is the primary international standard for utility billing integration and is explicitly extended to water and gas metering.

| Standard | Title | Relevance |
|----------|-------|-----------|
| IEC 61968-9:2024 | Application Integration at Electric Utilities – Meter Reading and Control | Specifies the CIM message types for meter reading, controls, events, customer data synchronisation, and switching for electric, gas, and water metering systems. Directly applicable to AMI/MDM-to-billing integration. |
| IEC 61968-11 | Application Integration at Electric Utilities – Common Information Model Extensions | Extends the CIM to cover asset tracking, work scheduling, and customer billing across utility types including water. |
| IEC 61970-301 | Energy Management System Application Program Interface (EMS-API) – Common Information Model (CIM) Base | Defines the foundational CIM object model underpinning IEC 61968; billing systems that interface with MDM or GIS systems may reference this model. |

IEC 61968-9:2024: https://webstore.iec.ch/en/publication/75041
IEC 61968 overview: https://en.wikipedia.org/wiki/IEC_61968

---

### MultiSpeak Specification

MultiSpeak is the most widely adopted de facto data-exchange standard for distribution utilities in North America, covering the interfaces between billing, metering, work management, and GIS systems.

| Specification | Relevance |
|---------------|-----------|
| MultiSpeak v5 (current) | Defines XML-based web-service interfaces for customer billing and PAN management, meter reading, AMI data exchange, work orders, and outage management. Over 90 vendors actively implement it. Billing systems integrating with AMI head-end systems should declare MultiSpeak compliance. |

MultiSpeak home page: https://www.multispeak.org/
What is MultiSpeak: https://www.multispeak.org/what-is-multispeak/

---

### W3C & IETF Standards

| Standard | Relevance |
|----------|-----------|
| RFC 9110 – HTTP Semantics | Foundation for all REST API design in billing system integrations; defines request/response semantics, status codes, and caching. |
| RFC 8288 – Web Linking | Defines the `Link` header used in paginated REST APIs — relevant to billing API responses returning large meter-reading or invoice datasets. |
| RFC 7519 – JSON Web Token (JWT) | Widely used for API authentication tokens issued by billing system OAuth servers. |
| RFC 6749 – OAuth 2.0 Authorization Framework | Standard for delegated authorisation in customer portal and third-party payment integrations. |
| RFC 7591 – OAuth 2.0 Dynamic Client Registration | Relevant for utility billing platforms exposing APIs to third-party apps and payment gateways. |
| W3C WCAG 2.1 | Web Content Accessibility Guidelines — applicable to customer-facing billing portal and self-service payment UIs. |

---

### Green Button / ESPI Data Standard

The ESPI (Energy Services Provider Interface) standard, marketed as Green Button, provides a standardised XML format and REST data-exchange protocol for sharing customer usage and billing data from utilities to customers and authorised third parties.

| Specification | Relevance |
|---------------|-----------|
| ESPI / Green Button Connect My Data | Provides a standardised way for customers to authorise third-party apps to access their water-usage and billing data from the utility. The standard is extendable to water and gas (currently dominated by electricity). Implementing Green Button-compatible data export positions a water billing platform for future data-portability mandates. |

Green Button at US Dept. of Energy: https://www.energy.gov/data/green-button
Green Button Alliance standard page: https://www.greenbuttonalliance.org/green-button
NIST Green Button introduction: https://www.nist.gov/system/files/documents/smartgrid/Green-Button-Initiative-051112.pdf

---

### Data Model & API Specifications

| Specification | Relevance |
|---------------|-----------|
| OpenAPI 3.1 | De facto standard for documenting REST APIs. A water billing platform should publish an OpenAPI spec for its billing, account, and meter-reading APIs to enable third-party integrations. |
| JSON Schema (Draft 2020-12) | Used to validate request and response payloads in billing APIs (invoice objects, meter-read records, account structures). |
| GeoJSON (RFC 7946) | Standard format for encoding service-point and meter location data exchanged with GIS systems. |
| CSV / ANSI X12 EDI | Legacy formats commonly used for batch meter-reading data exchange with AMR systems; billing platforms must support import from both. |

---

### Payment Processing Standards

| Standard | Relevance |
|----------|-----------|
| PCI DSS v4.0.1 | Payment Card Industry Data Security Standard — mandatory for any billing system that processes card payments. Requires encryption in transit (TLS 1.2+) and at rest, API security controls, tokenisation, and hosted payment page options to reduce scope. |
| NACHA Operating Rules | Governs ACH (eCheck/bank debit) payment processing. Water utilities commonly offer ACH autopay; NACHA rules mandate account validation, fraud-prevention controls, and transaction-type codes (WEB, PPD, CCD) appropriate to billing use cases. |
| ISO 20022 | International standard for financial messaging; increasingly used by banks for payment instruction formatting. |

PCI Security Standards Council: https://www.pcisecuritystandards.org/standards/
NACHA Operating Rules overview: https://www.nacha.org/content/how-ach-payments-work

---

### Security & Compliance Standards

| Standard | Relevance |
|----------|-----------|
| NIST SP 800-53 | Security controls catalogue referenced by US public utilities for system and communication protection. |
| OWASP API Security Top 10 (2023) | Defines the most critical API vulnerabilities — directly applicable to securing billing REST APIs, payment endpoints, and customer portal backends. |
| SOC 2 Type II | Cloud service trust standard; SaaS billing platforms serving municipal utilities are increasingly expected to hold SOC 2 Type II certification. |
| GDPR / State Privacy Laws (CCPA, etc.) | Customer name, address, usage data, and payment history qualify as personal data under GDPR (for EU-adjacent deployments) and US state privacy laws; billing systems must support data-subject access requests and retention limits. |

OWASP API Security: https://owasp.org/www-project-api-security/

---

## Similar Products — Developer Documentation & APIs

### Oracle Utilities Customer Care and Billing Cloud Service (CCS)

- **Description:** Enterprise CIS for large water, electric, and gas utilities covering meter-to-cash billing, customer care, service orders, and outage management.
- **API Documentation:** https://docs.oracle.com/en/industries/energy-water/customer-care-billing/index.html
- **SDKs/Libraries:** Oracle Integration Cloud; no standalone SDK. REST APIs available in CCS.
- **Developer Guide:** https://docs.oracle.com/en/industries/energy-water/customer-care-billing/
- **Standards:** REST/JSON, IEC 61968 CIM, OpenAPI
- **Authentication:** OAuth 2.0 (Oracle Identity Cloud Service)

---

### Bynry SMART360

- **Description:** AI-native cloud platform for SMB water, gas, and electric utilities with 25+ pre-built AMI integrations, automated meter-to-cash billing, and generative AI reporting.
- **API Documentation:** Available via Bynry support — not publicly indexed.
- **SDKs/Libraries:** Not publicly documented; AWS-hosted REST API.
- **Developer Guide:** https://www.bynry.com/features/utility-billing-software
- **Standards:** REST/JSON; AMI head-end adapters (Sensus, Itron, Neptune, Badger, Landis+Gyr)
- **Authentication:** Not publicly specified

---

### VertexOne VXcis / WaterSmart

- **Description:** Enterprise SaaS CIS and customer engagement platform for water utilities, offering billing, MDM, mobile workforce management, and water-analytics.
- **API Documentation:** https://www.vertexone.net/products/vxenterprise (contact for developer access)
- **SDKs/Libraries:** Not publicly documented.
- **Developer Guide:** https://www.vertexone.ai/
- **Standards:** REST/JSON; integrates with AMI, MDM, and GIS via standard interfaces
- **Authentication:** OAuth 2.0 (enterprise SSO)

---

### Muni-Link

- **Description:** Cloud-based utility billing SaaS for municipalities and boroughs; supports water, sewer, and multi-service billing with customer portal and mobile apps.
- **API Documentation:** https://muni-link.com/products/utility-billing-software/integrations-made-simple/
- **SDKs/Libraries:** Android and iOS mobile apps available.
- **Developer Guide:** Via integration page (contact required for API access)
- **Standards:** REST/JSON; AMR/AMI import; CASS address certification
- **Authentication:** Not publicly specified

---

### Springbrook (Accela)

- **Description:** Municipal ERP with utility billing module for water, sewer, and stormwater; includes real-time GL integration and allocation billing.
- **API Documentation:** https://springbrooksoftware.com (integration details via sales)
- **SDKs/Libraries:** Not publicly documented.
- **Developer Guide:** https://springbrooksoftware.com/solutions/utility-billing/
- **Standards:** REST/JSON for Cirrus SaaS platform; AMI/AMR adapters built-in
- **Authentication:** Enterprise SSO / role-based access

---

### AMCS Utility Billing

- **Description:** Affordable SaaS CIS for small-to-mid-market water, sewer, and electricity utilities; includes configurable rate structures, SMS reminders, and customer portal.
- **API Documentation:** https://www.amcsgroup.com/solutions/utility-billing/ (contact required)
- **SDKs/Libraries:** Not publicly documented.
- **Developer Guide:** Via SoftwareAdvice/Capterra listings for feature reference
- **Standards:** REST/JSON
- **Authentication:** Not publicly specified

---

### ACI Worldwide (Payment Processing for Utilities)

- **Description:** Payment-processing platform used by water and other utilities for online bill payment, ACH, card processing, and IVR payments; PCI-DSS compliant hosted payment pages.
- **API Documentation:** https://www.aciworldwide.com/solutions/pci-compliance-solutions
- **SDKs/Libraries:** REST APIs and hosted payment page (iframe) integration
- **Developer Guide:** Available via ACI developer portal (contact required)
- **Standards:** PCI DSS v4.0.1, NACHA ACH, ISO 20022, REST/JSON
- **Authentication:** API keys + TLS mutual auth

---

### Stripe (Payment Gateway — General Purpose)

- **Description:** General-purpose payment gateway widely used for utility customer portals; supports ACH, cards, and recurring billing with PCI DSS scope reduction via hosted elements.
- **API Documentation:** https://docs.stripe.com/api
- **SDKs/Libraries:** JavaScript, Python, Ruby, PHP, Go, Java, .NET — https://docs.stripe.com/libraries
- **Developer Guide:** https://docs.stripe.com
- **Standards:** PCI DSS SAQ A (hosted fields), NACHA ACH via Stripe Financial Connections, REST/JSON, OpenAPI
- **Authentication:** API keys (publishable + secret); webhook signing via HMAC-SHA256

---

## Notes

- **MultiSpeak vs. IEC 61968**: In North America, MultiSpeak dominates as the de facto standard for utility systems integration (billing ↔ AMI ↔ GIS ↔ work orders). IEC 61968 (CIM) is the international standard and is increasingly referenced in MDM and enterprise CIS implementations. An open-source billing platform should aim to support both.

- **Green Button for water**: ESPI/Green Button was developed for electricity but the specification explicitly supports extension to water. Implementing a Green Button-compatible data export endpoint would be a differentiator for customer data transparency.

- **Open API gap**: No water utility billing vendor publicly exposes a full OpenAPI specification. This is a meaningful opportunity for an open-source project to set the interoperability standard for the space.

- **Emerging standards**: The Water Information Sharing and Analysis Center (WaterISAC) and AWWA publish cybersecurity guidance (e.g., AWWA Cybersecurity Guidance for the Water Sector) that is increasingly relevant as utility billing systems become cloud-based and internet-facing. Consult https://www.awwa.org for current publications.
