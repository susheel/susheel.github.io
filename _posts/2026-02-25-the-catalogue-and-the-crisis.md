---
title: "The Catalogue and the Crisis"
layout: post
date: 2026-02-25 09:00
category: blog
author: susheel
tag:
- health data
- governance
- TRE
- open science
- HDRS
- Bermuda Principles
- federation
image: /assets/images/blog/opentre-uk/hero-panizzi.jpg
headerImage: true
description: "Why the UK's 600 million pound investment needs protocols, not another platform."
---

**Why the UK's 600 Million Pound Investment Needs Protocols, Not Another Platform**

*~30 min read*

---

> **OpenTRE**
>
> This is part of a series of papers arguing that the UK's health data infrastructure should build protocols, not services. Companion papers covering the full technical case, a visual executive summary, the political and rights-based vision, an enforceable rights framework, a protocol specification, and an implementation roadmap are available at [opentre.org](https://opentre.org/). For the US perspective, see [*The Current Wars of Biomedical Data*](https://opentre.org/us-blog.html).

---

### In 60 Seconds

**What:** OpenTRE proposes that the HDRS invest its 600 million pounds in open interoperability protocols (shared cataloguing rules for health data) rather than another centrally operated platform.

**Why:** The UK has spent over two decades and billions of pounds on centralised health data programmes (NPfIT, care.data, GPDPR, FDP) that follow the same pattern: centralise, meet resistance, retreat, rebrand. The problem is not technology. It is the absence of shared rules.

**What should be done now:** Six Bermuda-style mandates (24-hour governance disclosure, federated-first presumption, protocol conformance, credential portability, reciprocal contribution, and patient collective voice) would give the HDRS a durable foundation that survives political cycles.

---

<details>
<summary><strong>Key Terms and Acronyms</strong></summary>

**DARE UK**: Data and Analytics Research Environments UK. A UKRI programme building national TRE infrastructure.

**DUO**: Data Use Ontology. A GA4GH standard for machine-readable data use conditions.

**FDP**: Federated Data Platform. NHS England's 330 million pound data analytics platform operated by Palantir.

**FHIR**: Fast Healthcare Interoperability Resources. An HL7 standard for exchanging healthcare information electronically.

**GA4GH**: Global Alliance for Genomics and Health. An international standards body for genomic and health data sharing.

**HDRS**: Health Data Research Service. The UK government's 600 million pound programme to improve health data access for research.

**NDL**: National Data Library. A cross-sector UK government programme (over 100 million pounds) led by DSIT to make public data accessible for research, public services, and AI development.

**NPfIT**: National Programme for IT. The 12.7 billion pound NHS IT programme (2002-2011), largely abandoned.

**ODRL**: Open Digital Rights Language. A W3C standard for expressing permissions and obligations over data.

**OHDSI**: Observational Health Data Sciences and Informatics. A multi-stakeholder network using the OMOP model across 88 countries.

**OMOP**: Observational Medical Outcomes Partnership Common Data Model. A standardised schema for health data.

**SATRE**: Standard Architecture for Trusted Research Environments. A UK specification for TRE design, developed by DARE UK.

**SDE**: Secure Data Environment. The NHS-specific term for a TRE within the NHS ecosystem.

**TRE**: Trusted Research Environment. A secure computing facility where approved researchers analyse sensitive data without the data leaving the facility.

</details>

---

## The Catalogue and the Crisis

A clinical researcher at University College London is studying antibiotic resistance patterns across three regions of England. The data she needs exists in three separate Secure Data Environments. She has ethics approval. She has funding. She has a clear research question. What she does not have is a way to query across all three environments without negotiating a separate data access agreement with each one, a process that will take, by her own estimate, between nine and fourteen months per SDE. By the time she can run the analysis, her grant will have expired. This is exactly the kind of problem [OpenSAFELY](https://www.opensafely.org/) solved during COVID-19: code travelling to 58 million GP records rather than records travelling to researchers. The architecture works. The governance interoperability does not yet exist.

This is not a technology problem. It is a cataloguing problem. The data exists. The shared rules for accessing it do not. The same problem existed in the library world before 1841, when a political refugee published the rules that eventually connected every library on earth.

> **Why this matters for the HDRS**
>
> - **The pattern is identical:** before Panizzi, every library was an island with its own catalogue. Today, every NHS SDE is an island with its own governance process. The 600 million pound HDRS can write the shared rules, or build another island.
> - **Metadata travels, content stays:** Panizzi's rules standardised how to describe a book, not the book itself. OpenTRE standardises how to describe data access conditions, not the patient data. The "book" never leaves the shelf.
> - **Sovereignty is preserved:** no library surrendered its collection. No NHS Trust needs to surrender its data. Only the catalogue entries (the governance interfaces) need to conform.

In 1823, a young Italian revolutionary named Antonio Panizzi arrived in England. He had been sentenced to death in absentia for conspiracy against the Duke of Modena. He spoke little English. He had no money, no connections, and no prospects. Within fourteen years he would become Keeper of Printed Books at the British Museum Library, and in 1841 he would publish [91 cataloguing rules](https://www.britannica.com/biography/Anthony-Panizzi) that became the foundation of every library interoperability standard that followed.

Before Panizzi, every library was an island. Each institution catalogued its holdings in its own way, using its own conventions, its own entry formats, its own filing logic. A scholar who could navigate the Bodleian's catalogue was lost in the British Museum's. Finding a book meant knowing the local system. There was no shared language for describing what a library held.

Panizzi's insight was that the problem was not the buildings or the collections. The problem was the absence of shared rules. His 91 rules specified how to record an author's name, how to handle anonymous works, how to cross-reference editions, how to standardise titles. They were, in modern terms, a protocol: a set of agreements about representation that allowed any two institutions to understand each other's holdings without merging their collections.

The rules did not require libraries to reorganise their shelves, rebuild their reading rooms, or surrender their collections to a central repository. Each library kept its own governance, its own physical arrangements, its own traditions. Only the catalogue entries (the metadata describing what was held and how to find it) needed to conform to a shared standard. The books themselves never left the shelf. A scholar could discover what existed anywhere; the sensitive content stayed where it belonged. In OpenTRE's terms: the catalogue (governance metadata) travels; the patient data (the book) never does.

That lineage is direct and unbroken. Panizzi's rules (1841) led to Charles Ammi Cutter's [*Rules for a Dictionary Catalog*](https://www.britannica.com/biography/Charles-Ammi-Cutter) (1876) and, in the same year, Melvil Dewey's [Decimal Classification](https://www.oclc.org/en/dewey.html), which gave every library a shared language for organising knowledge by subject. Cutter standardised how to describe a book; Dewey standardised where to put it. Together they solved both halves of the interoperability problem. That dual tradition led to the [Anglo-American Cataloguing Rules](https://www.aacr2.org/) (1967) and to [Henriette Avram](https://www.loc.gov/marc/)'s MARC format at the Library of Congress (1966), which gave cataloguing a machine-readable encoding. MARC led to [Z39.50](https://www.loc.gov/z3950/agency/), the federated query protocol that lets a researcher in London search the catalogue of a library in Tokyo without either institution surrendering its data. Z39.50 led to [WorldCat](https://www.worldcat.org/), a federated discovery catalogue spanning tens of thousands of libraries across 170 countries. And the entire system rests on persistent identifiers like [ISBN](https://www.isbn-international.org/) and [ISSN](https://www.issn.org/), which let any catalogue entry point unambiguously to the same work.

A political refugee wrote the rules that let every library in the world talk to each other. No central warehouse was required. No single institution controlled the system. The protocol was the agreement. Everything else was implementation.

I find myself thinking about Panizzi's rules as I watch the UK prepare to spend 600 million pounds on a [Health Data Research Service](https://www.gov.uk/government/news/prime-minister-turbocharges-medical-research). The NHS has a cataloguing problem. Institutions that hold health data are essentially running incompatible catalogues: bespoke governance agreements, variable access processes, months-long negotiations, each request treated as a unique transaction. The data exists. The shared rules do not.

Panizzi built the Round Reading Room and expanded the collection, but his lasting contribution was the 91 rules that made every catalogue interoperable. The UK's health data infrastructure needs the same kind of reform.

The [Health Data Research Gateway](https://healthdatagateway.org/), which we built at [HDR UK](https://hdruk.ac.uk/), was the first metadata catalogue of health research datasets across all four UK nations. We also began aligning governance processes by developing a unified Data Access Request process using the Five Safes framework. Without a political mandate, however, uptake has been hard. The challenge of interoperable governance remains.

> **Key Takeaway**
>
> Panizzi understood that a library's value lies not in its collection but in the rules that make the collection usable. The NHS faces the same question: the HDRS should fund cataloguing rules, not another building.

> **Key Takeaway**
>
> The NHS has a cataloguing problem, not a technology problem. Shared rules for describing data access conditions, not more buildings, are what connect institutions.

---

*This is an excerpt of the full article. Read the complete version at [opentre.org/uk-blog.html](https://opentre.org/uk-blog.html).*

---

### About the Author

*[Susheel Varma](https://susheelvarma.com) is Chief Data Officer at [Sage Bionetworks](https://sagebionetworks.org) and was previously Chief Technology Officer at [Health Data Research UK](https://hdruk.ac.uk/), where he co-authored the [TRE Green Paper](https://doi.org/10.5281/zenodo.4594704) and [Building Trusted Research Environments](https://doi.org/10.5281/zenodo.5767586) guidance.*

*This is the UK perspective in a two-part series. For the US companion on why biomedical data portals need protocol infrastructure, read [The Current Wars of Biomedical Data](https://opentre.org/us-blog.html).*

---

Copyright 2026 Susheel Varma. Licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
