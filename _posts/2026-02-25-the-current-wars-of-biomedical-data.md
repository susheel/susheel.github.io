---
title: "The Current Wars of Biomedical Data"
layout: post
date: 2026-02-25 10:00
category: blog
author: susheel
tag:
- health data
- governance
- open science
- NIH
- biomedical research
- federation
- Bermuda Principles
image: /assets/images/blog/opentre-us/current-wars-v2.jpg
headerImage: true
original_url: "https://opentre.org/us-blog"
original_site: "OpenTRE"
description: "Why America's $48 billion biomedical research enterprise needs protocols, not more portals."
---

**Why America's $48 Billion Biomedical Research Enterprise Needs Protocols, Not More Portals**

*~30 min read*

---

> **OpenTRE**
>
> This is the US companion to [*The Catalogue and the Crisis*](https://opentre.org/uk-blog.html), which makes the case for protocol-based federation in the UK's NHS. This piece tells the same structural story from the perspective of US biomedical research. A different system, the same architectural trap.
>
> Both essays are part of the [OpenTRE paper suite](https://opentre.org), which includes a policy blueprint, technical specification, manifesto, bill of rights, and implementation roadmap.

---

### In 60 Seconds

**What:** OpenTRE proposes a shared protocol layer (identity, governance, analytics, and discovery) that lets existing NIH-funded platforms interoperate without replacing any of them.

**Why:** The US has invested tens of billions in biomedical data platforms that cannot talk to each other, costing researchers months of duplicated access negotiations and leaving cross-cutting scientific questions unanswerable.

**What should be done now:** NIH should require GA4GH Passport compliance and machine-readable governance in all new data platform grants: a protocol mandate that can begin within existing appropriations by redirecting current platform spend, protecting every dollar already invested.

---

<details>
<summary>Key Terms and Acronyms</summary>

- **TRE**: Trusted Research Environment: a secure computing space where approved researchers analyse sensitive data without the data leaving the environment.
- **OMOP**: Observational Medical Outcomes Partnership Common Data Model: a standard schema for representing clinical data so queries work across institutions.
- **FHIR**: Fast Healthcare Interoperability Resources: an HL7 standard for exchanging healthcare information electronically.
- **GA4GH**: Global Alliance for Genomics and Health: an international standards body for genomic and health data sharing.
- **ODRL**: Open Digital Rights Language: a W3C standard for expressing data use policies in machine-readable form.
- **DUO**: Data Use Ontology: a GA4GH standard vocabulary for encoding consent-based data use conditions.
- **OHDSI**: Observational Health Data Sciences and Informatics: a global network running federated analytics on the OMOP model across 544 data sources.
- **N3C**: National COVID Cohort Collaborative: an NIH platform with 23M+ patient records, hosted on Palantir Foundry.
- **CFDE**: Common Fund Data Ecosystem: an NIH initiative to connect data across Common Fund programmes.
- **GREI**: Generalist Repository Ecosystem Initiative: an NIH programme aligning metadata across seven generalist repositories.
- **DMS Policy**: NIH Data Management and Sharing Policy (2023): the first NIH-wide mandate requiring funded researchers to share scientific data.
- **RAS**: Researcher Auth Service: NIH's national identity broker implementing GA4GH Passports.

</details>

---

## The Current Wars

In the 1880s, Thomas Edison and George Westinghouse fought the "[Current Wars](https://www.energy.gov/articles/war-currents-ac-vs-dc-power)," a bitter battle over how to electrify America. Edison championed direct current (DC): simple, local, and controlled by Edison's company. Westinghouse backed alternating current (AC): standardised interfaces, long-distance transmission, and an open market where anyone could build on the grid.

Edison's DC worked beautifully for a single city block. It could not scale. Every new neighbourhood needed its own power station, its own wiring, its own operator. AC, standardised through transformers and regulated through grid codes, could power a continent.

Edison fought dirty, publicly electrocuting animals to prove AC was dangerous. He lost anyway. The real history is more complex than this sketch. Tesla's polyphase motor and long-distance transmission advantages were the decisive technical factors. But the structural lesson endures. Edison lost not because AC was safer (it isn't, inherently), but because **regulated interoperability scales and proprietary control does not.**

AC won because of the transformer: a device that stepped voltage up for long-distance transmission and down again for local use, allowing any generator and any appliance to join the same grid. In today's biomedical research system, [GA4GH Passports](https://www.ga4gh.org/product/ga4gh-passports/) are the transformer: they step a researcher's credentials up into a portable, machine-verifiable format and step them down again at each platform, allowing any data repository and any analytics environment to join the same grid.

The Current Wars ended over a century ago, but their structural logic is playing out right now in US biomedical research, with an embarrassingly familiar problem: hundreds of data portals, each excellently engineered, none able to talk to each other. The world's most generously funded research system, where [NIH alone distributes over $48 billion annually](https://report.nih.gov/funding/nih-budget-and-spending-data-past-fiscal-years/budget), has produced a patchwork of DC power stations. Each portal lights up its own city block. None of them share a grid.

> **Key Takeaway**
>
> The US biomedical data system recapitulates the Current Wars: dozens of proprietary power stations, no shared grid. GA4GH Passports are the transformers that could connect them.

---

## The Landscape: $48 Billion, Forty Silos

### The mandate without infrastructure

In January 2023, the [**NIH Data Management and Sharing (DMS) Policy**](https://sharing.nih.gov/data-management-and-sharing-policy) took effect, the first NIH-wide mandate requiring all funded researchers to share scientific data. A major policy shift, and also, to put it bluntly, an unfunded mandate. No new money for repositories. No compliance infrastructure. No interoperability requirements. Thousands of Data Management and Sharing Plans have since been filed. Almost none of them are verifiable. The DMS Policy told researchers to share. It gave them nowhere coherent to share to.

### The catalogue without connections

The [**Common Fund Data Ecosystem (CFDE)**](https://commonfund.nih.gov/dataecosystem), representing roughly $50 to $100 million in total investment, was designed to connect data across Common Fund programmes. After years of work, it covers only 13 of approximately 40 Common Fund programmes. The CFDE portal enables discovery but not integration or federated analysis. Individual programme portals remain separate islands. Another DC power station, larger than most, but still wired for one neighbourhood.

The [**Generalist Repository Ecosystem Initiative (GREI)**](https://datascience.nih.gov/data-ecosystem/generalist-repository-ecosystem-initiative), now in its fourth year, has made real progress: seven generalist repositories (Dryad, Figshare, Dataverse, Zenodo, and others) aligned on metadata standards via schema.org. But metadata alignment is not data interoperability. You can find the dataset. You still cannot query across repositories or run federated analysis.

### The platform without a parachute

[**All of Us**](https://allofus.nih.gov/), NIH's flagship precision medicine programme, is a $1.455 billion authorised under the 21st Century Cures Act. It has enrolled over 804,000+ participants, with notable diversity: 45% from underrepresented backgrounds. Yet its budget has been volatile: from $541 million in FY2023 to $158 million proposed for FY2025, a 71% reduction. It is a centralised platform, not a federated one, and an HHS Office of Inspector General cybersecurity audit flagged unresolved vulnerabilities. A single programme, however well-funded, is brittle by design. When funding is cut, the platform and every pipeline built on it are at risk.

The [**National COVID Cohort Collaborative (N3C)**](https://ncats.nih.gov/n3c) was a pandemic success story: over 23 million patient records, 240+ contributing sites, 4,600+ registered researchers. But it runs on Palantir's Foundry platform under a contract exceeding $60 million. Researchers who built analytical pipelines on Foundry are now locked into Foundry. That is the trade-off N3C made: speed during a crisis, at the cost of independence afterwards.

### US Biomedical Data Landscape at a Glance

| Programme | What Works | Why It Does Not Federate | Structural Lesson |
|-----------|-----------|--------------------------|-------------------|
| **N3C** | 23M patient records; pandemic-speed assembly | Single-vendor platform (Palantir Foundry); pipelines locked in | Speed without open interfaces creates lock-in |
| **All of Us** | 804,000+ participants; 45% from underrepresented backgrounds | Centralised platform; budget volatility (71% proposed cut FY2025) | Centralised programmes are structurally fragile to budget cycles |
| **AMP** | $1B+ across disease areas; real science | Same consortium, three platforms, no credential portability | Even internal consortia silo without shared protocols |
| **OHDSI** | 974M records; 544 sources; 88 countries; no central warehouse | Governance and identity are out of scope; ETL burden on sites | Protocol-first design scales; missing layers are still missing |
| **CFDE** | Discovery across 13 Common Fund programmes | No integration or federated analysis; only 13 of ~40 programmes | Catalogues without query layers are incomplete |
| **GREI** | Seven repositories aligned on schema.org metadata | Surface-level alignment; no cross-repository query | Guidelines without protocols produce unverifiable compliance |
| **NCPI** | Connecting AnVIL, BioData Catalyst, CRDC, Kids First | Cross-platform queries remain experimental after years | Connecting platforms after the fact is harder than designing for interop |

None of these programmes is bad. Most of them are impressive. That is the frustration. Tens of billions invested, real science produced, and there is still no grid.

---

*This is an excerpt of the full article. Read the complete version at [opentre.org/us-blog.html](https://opentre.org/us-blog.html).*

---

### About the Author

[Susheel Varma](https://susheelvarma.com) is Chief Data Officer at [Sage Bionetworks](https://sagebionetworks.org) and was previously Chief Technology Officer at [Health Data Research UK](https://hdruk.ac.uk/), where he co-authored the [TRE Green Paper](https://doi.org/10.5281/zenodo.4594704) and [Building Trusted Research Environments](https://doi.org/10.5281/zenodo.5767586) guidance.

This is the US companion to [*The Catalogue and the Crisis*](https://opentre.org/uk-blog.html). For the UK perspective on protocols vs platforms, read the original piece.

---

*Copyright 2026 Susheel Varma. Licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).*
