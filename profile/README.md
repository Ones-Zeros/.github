<p align="center">
  <img src="https://onzdev.com/assets/logo_text-hSozmQYT.png" alt="Ones & Zeros Logo" width="180" />
</p>

<h1 align="center">Ones &amp; Zeros (Pvt) Ltd</h1>

<h3 align="center">Digital public infrastructure for agriculture and government services</h3>

<p align="center">
  We build national registries, benefit management systems, and the interoperability layers that connect them &mdash;<br/>
  in production today with the Food and Agriculture Organization of the United Nations across five countries.
</p>

<p align="center">
  <a href="https://onzdev.com/" target="_blank">
    <img src="https://img.shields.io/badge/Website-onzdev.com-111827?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website" />
  </a>
  <a href="mailto:info@onzdev.com">
    <img src="https://img.shields.io/badge/Email-info@onzdev.com-1f2937?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://www.linkedin.com/company/onesnzeros/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Ones%20%26%20Zeros-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Registered%20in-Sri%20Lanka-111827?style=flat-square" alt="Sri Lanka" />
  <img src="https://img.shields.io/badge/UN%20partner-FAO-009EDB?style=flat-square" alt="FAO" />
  <img src="https://img.shields.io/badge/Deployments-5%20countries-1f2937?style=flat-square" alt="Five countries" />
  <img src="https://img.shields.io/badge/Digital%20Public%20Good-in%20preparation-2E7D32?style=flat-square" alt="Digital Public Good in preparation" />
</p>

---

## What we actually do

Most software companies describe what they *can* build. This page describes what we have **built, tested with government users, and handed over**.

Ones &amp; Zeros designs and operates the systems that let a government answer three questions authoritatively: **who its farmers are, what they produce, and who has already received which benefit.** That means registries that hold identity, mobile applications that work where there is no network, API gateways that let other institutions consume the data without copying it, and the migration and training work that gets a real institution onto the system.

We work almost entirely on donor-funded and public-sector programmes, where the delivery bar is acceptance testing with real officers, documented handover, and a system that still runs after the consultants leave.

---

## Track record at a glance

| | |
|---|---|
| **Countries with production deployments** | 5 &mdash; Sri Lanka, Tonga, Cook Islands, Solomon Islands, Vanuatu |
| **Government &amp; institutional systems delivered** | 7 |
| **Primary client** | Food and Agriculture Organization of the United Nations (FAO Sri Lanka &amp; Maldives, FAO Subregional Office for the Pacific) |
| **Sri Lankan institutions served** | Department of Agriculture · Department of Export Agriculture · Department of Cinnamon Development |
| **Core team** | 7 permanent engineers; technical leadership with 13+ years, senior engineers with 10+ years |
| **Delivery model** | Fixed-scope milestone delivery, UAT sign-off, train-the-trainer handover, source and documentation transferred to the client |

---

## Flagship platform &mdash; Digital Farmer Registry (DFR)

A multi-country farmer registration and management platform built for FAO and deployed for **Tonga, the Cook Islands, the Solomon Islands and Vanuatu** under a single programme. Each country runs its own instance &mdash; own branding, languages, administrative hierarchy and form catalogue &mdash; on one shared codebase.

**What is in the platform**

- **Offline-first mobile enumerator application (Flutter)** &mdash; officers log in, download an assignment, register farmers, complete forms, capture GPS points and draw plot polygons with no network connection, then synchronise through a defined state machine. Offline map regions, review-and-approve chain, on-device diagnostics.
- **No-code dynamic form builder** &mdash; ministries change their own registration forms on a design canvas without a release.
- **Identity and access layer (Keycloak)** &mdash; role-based access control, federation-ready.
- **Approval workflow engine** &mdash; submission review, multi-level approval, full audit trail on every record.
- **Farmer self-service portal** and administrator console.
- **Unified data import framework** &mdash; legacy registry migration with de-duplication and validation.
- **Dashboards and reporting** over the registry data.

Every country instance passed user acceptance testing conducted by national ministry staff, with test evidence, defect tracking and formal sign-off before production deployment, and was handed over with a role-specific train-the-trainer programme for administrator, farmer and enumerator roles.

### Digital Public Good preparation

The DFR codebase is being prepared for classification as a **Digital Public Good** under the FAO Digital Assets Management Standard and the DPG Standard.

- **Milestone 1 of 4 complete** &mdash; full security and compliance assessment across backend, web and mobile (OWASP Dependency-Check on the Java/Spring backend, `npm audit` on the Next.js frontend, MobSF static analysis on the Flutter Android release), with a mapped gap analysis and a dated, resourced remediation plan presented to the FAO Digital Empowerment team.
- Being prepared for release at the **Pacific Region Digital Agriculture Forum, Solomon Islands, 1&ndash;6 November 2026**.
- For adopting governments this means no licence cost, no vendor lock-in, an OSI-approved licence, and a codebase that improves with every country that joins it.

---

## Programme portfolio

### CROPIX &mdash; national e-Agriculture platform
**Client:** FAO Sri Lanka / Department of Agriculture. Crop registry, operational workflows, field data collection, reporting and decision support for the national agriculture sector, with an administrative web system and connected mobile application.

### Sector API Gateway and Interoperability Layer
**Client:** FAO Sri Lanka / Department of Agriculture. The exchange layer that lets sector institutions consume authoritative registry data through governed APIs instead of maintaining their own copies &mdash; built to the registry-based distributed model set out in the Sri Lanka Government Agriculture Enterprise Architecture.

### GAP Certification Management System
**Clients:** Department of Agriculture · Department of Export Agriculture · Department of Cinnamon Development. Good Agricultural Practices certification lifecycle &mdash; application, inspection, audit, certificate issue and renewal &mdash; the system that stands between a smallholder and export market access.

### Project Activity Reporting Platform &amp; Decision Support Suite
**Client:** FAO. Programme monitoring, activity reporting and management decision support, proven at a UN agency across two countries and domain-agnostic by design.

### Agri-Advisory Platform
Digital extension and advisory delivery to farmers, connected to the registry so advice reaches the right cultivator on the right plot.

### Beyond agriculture
Institutional and enterprise systems including work for the Sri Lanka College of Oncologists, alongside 20+ commercial web and mobile delivery engagements.

---

## How we build

The things that decide whether a public-sector system survives its first year:

- **Offline-first, not offline-tolerant.** Field officers work where connectivity does not exist. Synchronisation is designed as a state machine, not retried as an afterthought.
- **Registry-based architecture.** One authoritative source per data domain, exposed through a gateway. No shadow copies, no reconciliation problem later.
- **Policy enforced as code.** Data sharing rules evaluated at the gateway on every request and written to an immutable audit record &mdash; not left as a document nobody can enforce.
- **Continuous security, not a point-in-time certificate.** Dependency, package and mobile static analysis wired into CI, because a stack of Spring, Next.js, Flutter and the Android SDK does not stay compliant on its own.
- **Traceability to requirement.** Every specification clause maps to the deliverable section that answers it, issued with the deliverable so the client can verify coverage directly.
- **Handover as a deliverable.** Source, deployment artefacts, documentation, and role-specific training. The client is never dependent on us to continue the work.

---

## Standards and interoperability

<p align="center">
  <img src="https://img.shields.io/badge/SL--GAEA-Agriculture%20Enterprise%20Architecture-111827?style=flat-square" alt="SL-GAEA" />
  <img src="https://img.shields.io/badge/SL--GAIF-Interoperability%20Framework-1f2937?style=flat-square" alt="SL-GAIF" />
  <img src="https://img.shields.io/badge/NDX-National%20Data%20Exchange-374151?style=flat-square" alt="NDX" />
  <img src="https://img.shields.io/badge/SL--UDI-Identity%20federation-4b5563?style=flat-square" alt="SL-UDI" />
  <img src="https://img.shields.io/badge/DPG%20Standard-Digital%20Public%20Goods-2E7D32?style=flat-square" alt="DPG Standard" />
  <img src="https://img.shields.io/badge/FAO-Digital%20Assets%20Management%20Standard-009EDB?style=flat-square" alt="FAO DAMS" />
</p>

Our architectures are designed for national data exchange and identity federation from the start, not retrofitted when the mandate arrives.

---

## Engineering stack

**Backend** &nbsp;
<img src="https://img.shields.io/badge/Java-111827?style=flat-square&logo=openjdk&logoColor=white" alt="Java" />
<img src="https://img.shields.io/badge/Spring%20Boot-1f2937?style=flat-square&logo=springboot&logoColor=6DB33F" alt="Spring Boot" />
<img src="https://img.shields.io/badge/REST%20%2F%20OpenAPI-374151?style=flat-square&logo=openapiinitiative&logoColor=white" alt="OpenAPI" />

**Web** &nbsp;
<img src="https://img.shields.io/badge/React-111827?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
<img src="https://img.shields.io/badge/Next.js-1f2937?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
<img src="https://img.shields.io/badge/TypeScript-374151?style=flat-square&logo=typescript&logoColor=3178C6" alt="TypeScript" />

**Mobile** &nbsp;
<img src="https://img.shields.io/badge/Flutter-111827?style=flat-square&logo=flutter&logoColor=54C5F8" alt="Flutter" />
<img src="https://img.shields.io/badge/Offline--first%20sync-1f2937?style=flat-square" alt="Offline-first sync" />

**Data &amp; geospatial** &nbsp;
<img src="https://img.shields.io/badge/PostgreSQL-111827?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
<img src="https://img.shields.io/badge/PostGIS-1f2937?style=flat-square&logo=postgis&logoColor=white" alt="PostGIS" />
<img src="https://img.shields.io/badge/MySQL-374151?style=flat-square&logo=mysql&logoColor=white" alt="MySQL" />

**Identity &amp; security** &nbsp;
<img src="https://img.shields.io/badge/Keycloak-111827?style=flat-square&logo=keycloak&logoColor=white" alt="Keycloak" />
<img src="https://img.shields.io/badge/OWASP%20Dependency--Check-1f2937?style=flat-square&logo=owasp&logoColor=white" alt="OWASP Dependency-Check" />
<img src="https://img.shields.io/badge/MobSF-374151?style=flat-square" alt="MobSF" />

**Platform &amp; delivery** &nbsp;
<img src="https://img.shields.io/badge/Docker-111827?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
<img src="https://img.shields.io/badge/Kubernetes-1f2937?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes" />
<img src="https://img.shields.io/badge/Azure-374151?style=flat-square&logo=microsoftazure&logoColor=white" alt="Azure" />
<img src="https://img.shields.io/badge/Google%20Cloud-4b5563?style=flat-square&logo=googlecloud&logoColor=white" alt="Google Cloud" />
<img src="https://img.shields.io/badge/AWS-111827?style=flat-square&logo=amazonwebservices&logoColor=white" alt="AWS" />
<img src="https://img.shields.io/badge/CI%2FCD-1f2937?style=flat-square&logo=githubactions&logoColor=white" alt="CI/CD" />

---

## Working with us

We take on assignments where the schedule is fixed and the system has to be real at the end of it. Typical engagement shapes:

| Engagement | What it looks like |
|---|---|
| **Country deployment of the DFR platform** | Configuration, extension, migration, UAT, training and handover &mdash; starting from a proven platform rather than an empty repository |
| **Registry and benefit management build** | Scheme registry, eligibility rules, entitlement ledger, disbursement and grievance workflows on top of an existing registry |
| **Interoperability &amp; API gateway work** | Governed data exchange, identity federation, machine-readable sharing policy, immutable audit |
| **Assessment &amp; re-engineering studies** | Institutional baseline assessment, business process re-engineering, digital strategy and implementation roadmaps |
| **Support &amp; managed operations** | Annual support and maintenance contracts with defined response commitments on systems we or others have built |

**Roles we field:** Project Manager · Solution Architect · Business Analyst · Senior Software Engineers · QA Lead and QA Engineers · DevOps / Cloud Engineer.

---

## Contact

<p align="center">
  <strong>Ones &amp; Zeros (Pvt) Ltd</strong> &mdash; Sri Lanka<br/>
  <a href="https://onzdev.com/">onzdev.com</a> &nbsp;·&nbsp;
  <a href="mailto:info@onzdev.com">info@onzdev.com</a> &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/company/onesnzeros/">LinkedIn</a> &nbsp;·&nbsp;
  <a href="https://www.facebook.com/onesnzerostec">Facebook</a>
</p>

<p align="center">
  <sub>Registered UN Global Marketplace vendor · Available for FAO, IFAD, World Bank and ADB funded assignments</sub>
</p>

<p align="center">
  <strong>Systems that a government still runs after the project closes.</strong>
</p>
