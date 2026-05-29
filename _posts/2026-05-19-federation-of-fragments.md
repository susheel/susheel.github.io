---
title: "The Federation of Fragments"
layout: post
date: 2026-05-19 09:00
category: blog
author: susheel
tag:
- health data
- governance
- HDRS
- TRE
- open science
- federation
description: "What Wellcome's Independent Review tells us about the HDRS and why the UK's health data infrastructure needs protocols, not services."
---

**What Wellcome's Independent Review Tells Us About the HDRS**

---

> **OpenTRE**
>
> This is part of a series of papers arguing that the UK's health data infrastructure should build protocols, not services. Companion papers covering the full technical case ([Blueprint](https://opentre.org/blueprint.html)), a visual executive summary ([Six Pages](https://opentre.org/sixpages.html)), the political and rights-based vision ([Manifesto](https://opentre.org/manifesto.html)), an enforceable rights framework ([Bill of Rights](https://opentre.org/rights.html)), a protocol specification ([Technical Specification](https://opentre.org/techspec.html)), and an implementation roadmap ([Roadmap](https://opentre.org/roadmap.html)) are available at [opentre.org](https://opentre.org/). For the original UK analysis, see [*The Catalogue and the Crisis*](https://opentre.org/uk-blog.html).

---

## The Catalogue Returns

In 1831, Antonio Panizzi arrived at the British Museum to find 240,000 books and no catalogue. The collection was large. What it lacked was the connective tissue that would let anyone find anything.

In May 2026, a team commissioned by Wellcome, Emrys Health, and Nesta published an independent review of the UK's health data infrastructure and found, essentially, the same problem at national scale. The report calls it a "federation of fragments" (p.39): 200-plus hospital trusts, 30-plus EHR vendors, four devolved nations, world-class individual data assets, and no integration architecture connecting them. The components exist. The connective layer does not.

This is the problem OpenTRE was designed to solve. And the report's findings, reached independently through semi-structured interviews with 78 stakeholders across 36 organisations, validation workshops in all four nations, and six concrete user stories, now provide the evidence base.

I helped build some of the systems this report reviews: the Health Data Research Gateway, the Five Safes data access request process, the TRE architecture standards. I left HDR UK in 2022. I published the OpenTRE argument in February 2026 at the Bermuda Principles 30th anniversary conference, using architectural reasoning, protocol design, and historical analogy. The Wellcome-commissioned team, working independently with different methodologies, arrived at the same diagnosis. That convergence matters, not because it validates my argument (though it does), but because two independent analyses using different methods reaching the same conclusion is the closest thing to replication that policy analysis offers.

The plagiarism assessment is clean. OpenTRE is not cited in the report. The report is not derivative of OpenTRE. The methodologies are different, the theoretical frameworks are different, and the distinctive elements of each document (OpenTRE's internet analogies and Bermuda mandates; the report's data fabric evaluation and user stories) are absent from the other. The convergence is on the diagnosis, not the framing. That makes it stronger evidence than either document alone.

---

## The Diagnosis, Layer by Layer

The report identifies five technology gaps across six infrastructure layers (Figure 6, p.40). Each of those gaps maps to specific layers in the OpenTRE protocol stack. The mapping is not forced. In several cases, the report uses language that is remarkably close to OpenTRE's formulations without using OpenTRE's terminology.

### Gap 1: No Minimum Information Standards

The report finds that "no minimum information standards define what a research data asset should contain" (p.39). The same data types are represented differently across assets. Standard vocabularies like dm+d and SNOMED CT subsets are applied inconsistently. Provenance documentation ranges from comprehensive to entirely absent.

This is OpenTRE's Layers 5 and 6: Interoperable Data and Data Quality Protocols. The individual standards exist. OMOP is deployed at 42 UK organisations across 81 data assets. FHIR is a ratified standard. SNOMED CT is mandated. The problem is that nobody has composed them into a specification with conformance levels. The report confirms what OpenTRE argues: having standards is not the same as having a protocol that requires them.

### Gap 2: Isolated Environments Without Integration

The report's strongest verdict lands here: asset integration is "the weakest layer relative to HDRS ambition" (p.42). Regional SDEs in England operate in isolation. Scottish Safe Havens lack automated federation. Welsh and Northern Irish infrastructure has no systematic connection to English or Scottish assets. The report states plainly that "no scalable integration architecture currently operates at population scale."

The report evaluates three architectural options for addressing this. Centralisation, where data moves to one place, faces the same governance obstacles that defeated NPfIT, care.data, and GPDPR: "previous UK attempts... encountered governance objections and public opposition, and a new centralised infrastructure may carry a similar inherent risk of failure" (p.42). Federated analytics, where computation moves to the data, works in specific contexts (DataSHIELD, OpenSAFELY, OMOP networks) but requires rigid schema conformance and excludes eyes-on data exploration. Data fabric, a metadata-driven approach that allows incremental adoption without a universal schema, has no mature UK implementation.

The report recommends a hybrid: "federated mechanisms for discovery and feasibility queries where OMOP-standardised networks exist, while enabling combined analysis in TREs for use cases requiring eyes-on access" (p.44).

This is the core of OpenTRE's architectural argument. The seven-layer protocol stack is, in effect, the specification for what the report calls the "integration layer." The report's endorsement of a hybrid approach that builds on open standards rather than proprietary platforms, and defines "technical specifications that participating assets must meet" (p.44), is protocol-like thinking expressed in operational language.

### Gap 3: Unreliable Data Linkage

No mechanism exists to identify which data sources hold records for a given individual. Linkage quality is inconsistent, unmeasured, and unmonitored. Researchers cannot quantify linkage error or compare results across studies. The report calls for accredited linkage providers meeting common standards rather than a single national service.

This maps to OpenTRE's Layers 1 through 3: Trust Infrastructure, Interoperable Identities, and Interoperable Metadata. The report's call for "patient dataset resolution" parallels OpenTRE's metadata discovery layer.

### Gap 4: Variable TRE Capability

TRE quality varies substantially. Current accreditation through SATRE focuses on security but does not evaluate researcher needs: compute capability, statistical software availability, GPU access. The report notes a pharmaceutical company discovering after approval that a TRE lacked the specified statistical software, and an AI developer finding no GPU capability.

This maps to OpenTRE's Layer 7 (Interoperable Infrastructure) and the conformance testing framework. The report's acknowledgement that security-only accreditation is insufficient validates OpenTRE's broader conformance model, where accreditation must address usability alongside security.

### Gap 5: Governance as the Key Barrier

And then we arrive at the gap that matters most, the one where convergence between the report and OpenTRE is closest.

The report documents governance that is "fragmented, manual, and opaque" (p.47). Identical work is repeated across organisations. Timelines are unpredictable. A researcher applying to multiple data controllers faces "separate documentation in different formats, credentials not recognised across controllers, and institutional agreements requiring renegotiation" (p.48). Progress is tracked through "emails, conversations, and spreadsheets" (p.35). "Approvals in one system are not visible in another" (p.47). Governance operates "sequentially rather than in parallel" (p.36): a Data Access Committee can reject a study after it has received ethics and CAG approvals.

One study reported 2.5 years from setup to data acquisition (p.36). The Safe People Registry, which should provide portable researcher credentials, is "under-invested and not universally recognised" (p.48).

The report's Opportunity 5 calls for a "unified digital governance layer" with three components: portable researcher credentials, reusable machine-readable agreement templates, and transparent project lifecycle tracking (p.48).

Those three components map directly to OpenTRE's Layer 4 (Interoperable Governance). Portable credentials map to W3C Verifiable Credentials and GA4GH Passports. Reusable machine-readable templates map to ODRL policies and Five Safes as code. Lifecycle tracking maps to the protocol ecosystem's audit trail. The report arrived at this through empirical gap analysis, interviewing stakeholders who said governance is the biggest barrier. OpenTRE arrived at it through architectural reasoning, placing governance at the thin waist of an hourglass protocol stack. Different methods, same destination.

---

## Opportunity 5: The Governance Layer

Opportunity 5 deserves particular attention because it is the report's closest match to what OpenTRE proposes, and because it is where the report's own framing introduces a phrase worth taking seriously.

The report calls for a transition from a "trust and contracts" model to a "technology guarantee" model (p.39). That phrase restates OpenTRE's "protocols, not services" in language that policy audiences will find actionable. Trust and contracts is the bilateral-agreement world: every data access negotiated from scratch, every credential re-verified, every timeline uncertain. A technology guarantee is a world where the system enforces standards computationally: if your credentials meet the published specification, access is granted; if your TRE meets the conformance standard, it participates in the network.

The report decomposes this into three components that map precisely to OpenTRE:

**Portable credentials.** The report documents that researcher credentials verified and accepted by one data controller are not recognised by the next. OpenTRE's third mandate, credential portability, addresses this through GA4GH Passport-compatible infrastructure. A researcher approved by any conformant TRE should be recognised by all others.

**Machine-readable agreement templates.** The report calls for reusable templates that reduce the "bespoke burden" of over 100 individual negotiations (p.36-37). OpenTRE's Layer 4 specifies how this works: ODRL policies encoding the Five Safes framework in a machine-readable format, so that access conditions can be matched computationally rather than negotiated bilaterally.

**Lifecycle tracking.** The report documents that project progress is tracked through emails and spreadsheets, with approvals in one system invisible to another. OpenTRE's protocol ecosystem includes audit trails and transparency logs as architectural requirements, not optional features.

Where the report and OpenTRE diverge is instructive. The report frames Opportunity 5 as a platform to be built, a "governance transaction platform" that HDRS would operate or commission. OpenTRE frames the same capability as a protocol to be adopted, a set of standards that any conformant TRE implements locally. The report's Pilot 5 (a governance transaction platform) is a service. OpenTRE's Layer 4 is a protocol. That distinction matters, because a centrally operated governance platform is one spending review away from defunding, while a protocol adopted across institutions survives political cycles.

---

## The Clinical Trials Crisis

The report deploys its most urgent data in the clinical trials section, and the numbers are damning.

The UK has dropped from 4th to 8th globally for Phase III clinical trials (p.7). Industry-sponsored trial enrolment hit 19,000 participants in 2024/25, a seven-year low (p.7). The UK is the second slowest of 18 European countries for trial setup (p.7). One major pharmaceutical company reported that the UK is slower than all but one European country. Industry stakeholders describe the UK, consistently and on the record, as "an unreliable and unpredictable partner" (p.36, p.51).

The government has set targets: 150-day trial setup by March 2026, quadrupled recruitment by 2029 (p.8). The economic stakes are substantial: the report estimates the HDRS could generate 3 billion pounds in gross value added, 485 million pounds in NHS revenue, and 26,000 jobs (p.8).

These targets are not achievable with the current governance architecture. A pharmaceutical company running a post-authorisation safety study across all four nations faces separate applications to multiple controllers, each with different forms, fees, and timelines. Feasibility tools query administrative data but cannot assess clinical depth: staging, biomarkers, treatment lines. For oncology trials, up to 90% of patients identified through current methods do not meet detailed eligibility criteria at pre-screening (p.51). The DigiTrials system, the current state of the art, is capped at approximately ten trials per year.

This is what bilateral governance costs. Every trial that takes 2.5 years to set up is a trial that runs in another country instead. Every credential that must be re-verified is a month lost. Every agreement negotiated from scratch is a quarter consumed by administration rather than recruitment.

The six federation mandates address this directly. Credential portability means a trial sponsor's credentials are verified once and recognised across all conformant TREs. Protocol conformance means every participating TRE meets published standards for data quality, compute capability, and governance interface. The federated-first presumption means trial data stays at the source institution, with only analytic queries and disclosure-checked results crossing boundaries. The patient rights dashboard means trial participants can see how their data contributed to the study. Reciprocal contribution means that institutions participating in trial infrastructure contribute back to the commons.

The clinical trials crisis is not a tangential concern. It is the most visible symptom of governance fragmentation, the one that costs jobs, investment, and patient outcomes. If the HDRS addresses nothing else, it should address this.

---

## What the HDRS Should Do Now

The report provides the evidence. OpenTRE provides the architecture. Here is what the six federation mandates look like when updated with the report's findings.

### 1. Federated-first presumption

The report endorses this implicitly by rejecting centralisation as the primary strategy and recommending "federated mechanisms for discovery and feasibility queries" (p.44). The mandate is straightforward: all HDRS-funded analysis runs at the data source by default. Code travels to data. Only aggregated, disclosure-checked results return. The report's own evaluation of the three architectural options makes this the least contentious mandate.

### 2. Protocol conformance

The report asks "what technical specifications for integration layer participation?" (p.44). OpenTRE's protocol stack answers this: GA4GH Passports for identity, OMOP for common data models, ODRL for machine-readable governance, SATRE-plus for TRE accreditation. The mandate requires all HDRS-funded infrastructure to implement these open standards and pass a published conformance test suite. The report's recommendation to "build on open standards rather than proprietary platforms" (p.44) is this mandate in policy language.

### 3. Credential portability

The report documents that portable credentials are the single most requested operational improvement across all stakeholder groups. The Safe People Registry exists but is "under-invested and not universally recognised" (p.48). The mandate: researcher credentials approved by any conformant TRE must be recognised by all others, via GA4GH Passport-compatible infrastructure. The report's Opportunity 5 and OpenTRE's third mandate converge on this without qualification.

### 4. Reciprocal contribution

The report's System Gap 2 (p.50) identifies the incentive problem: data controllers bear costs and risks without reliable mechanisms for fair return. Options include revenue sharing from commercial access, investment in local data engineering, access to validated tools, and benchmarking data. The mandate: every organisation that queries the federation contributes data, compute, or governance capacity back to the commons. The report's "value-return framework" is the operational expression of this principle.

### 5. Patient rights dashboard

The report's System Gap 3 (p.50) confirms that public trust is conditional and fragile. The National Data Opt-Out stands at 5.4%, spiking during trust crises. The report recommends "public-facing dashboards, searchable registries of approved projects, and feedback mechanisms that demonstrably influence decisions" (p.50) and cites Estonia's X-Road, where citizens can see exactly who accessed their data. The mandate: every data subject sees, in plain language, who accessed their data, for what purpose, and what was found. The report provides the evidence that this is not optional.

### 6. Patient collective voice

The report recommends "standing governance bodies with patient representation" (p.50) and its two PPIE sessions documented public demand for genuine decision-making authority, not merely transparency. The mandate: patient populations participate in federation governance through structured mechanisms, such as data trusts and standing citizens' panels, with genuine decision-making authority. The report's framing and OpenTRE's mandate are aligned.

---

## Where the Report Gets It Wrong

Independent validation does not mean uncritical endorsement. The report's own risk section deserves engagement, and there are points where its framing diverges from what the evidence supports.

### The service framing

The report consistently frames HDRS as a "service" with "customers" and "service level commitments." OpenTRE frames the solution as a "protocol" with "participants." These are fundamentally different institutional designs.

A service model implies a central provider delivering capability to consumers. A protocol model implies a shared set of rules that distributed participants implement locally. The report acknowledges that centralisation has repeatedly failed in UK health data, and then proposes a service architecture that structurally resembles centralisation. Opportunity 5 as a "governance transaction platform" operated by HDRS is a service. Layer 4 as a machine-readable governance protocol adopted by every conformant TRE is a protocol. The first is one spending review away from defunding. The second survives political cycles.

The report's service framing is understandable. Wellcome, HDRS, and the organisations interviewed think in service terms. The language is familiar to policymakers. But service thinking is what produced NPfIT, care.data, GPDPR, and the FDP. Protocol thinking is what produced the internet, email, and the OHDSI network. The UK's 600 million pounds should fund the latter.

### The central TRE option

The report evaluates a "central TRE" as a viable option (p.46-47), where HDRS would "operate an environment for deploying TREs." This reintroduces a single point of failure and vendor dependency. The British Library ransomware attack of October 2023, which took digital services offline for months, demonstrated what happens when everything is concentrated in one infrastructure. A protocol-based ecosystem distributes that risk.

There is a legitimate role for a reference implementation, a central TRE that demonstrates conformance and provides a fallback for institutions that lack local capability. But a reference implementation is different from a mandated central service. The first serves the network. The second requires the network to serve it.

### The "technology guarantee" ambiguity

The report's phrase "technology guarantee" is powerful but ambiguous. It could mean a protocol guarantee: if your system speaks the standard, it interoperates. Or it could mean a service guarantee: HDRS guarantees a certain level of capability. The first is distributed and resilient. The second is centralised and fragile.

OpenTRE's "protocols, not services" framing resolves this ambiguity. The guarantee should be that any conformant TRE can participate in the federation, not that HDRS operates the federation centrally. The guarantee lives in the protocol, not in the institution.

### Adoption risk

The report's most honest acknowledgement is that no mature UK example of a data fabric architecture exists at scale. This is real. OpenTRE's protocol stack is a design, not a deployed system. The gap between specification and implementation is where most health data programmes have failed.

The HDRS should address this through what OpenTRE calls success-based funding: funding institutions specifically to achieve protocol compliance, with payment tied to passing interoperability tests, not to shipping data upstream. The OHDSI network offers a model. Institutions bear the upfront cost of mapping to the common data model, then participate in every subsequent federated study at near-zero marginal cost. The UK needs Mapping-as-a-Service teams that do the heavy lifting for under-resourced NHS trusts.

---

## Convergence as Evidence

The Wellcome-commissioned report is the most thorough independent assessment of the UK's health data infrastructure published to date. It documents, with empirical rigour, the problems that OpenTRE was designed to address. The convergence between two independent analyses, one based on 78 stakeholder interviews and six user stories, the other based on architectural reasoning and protocol design, strengthens both.

The report provides what OpenTRE lacked: a comprehensive evidence base grounded in stakeholder testimony. OpenTRE provides what the report lacks: a prescriptive protocol architecture with published conformance levels, named standards, and an implementation pathway.

Together, they make a case that is difficult to dismiss. The UK's health data problem is not technology. It is the absence of shared rules. The components exist. The connective layer does not. Two independent teams have now said so.

The question is whether the HDRS will invest its 600 million pounds in writing the cataloguing rules, or in building another library.

---

**Write the cataloguing rules.**

[opentre.org](https://opentre.org)

---

### About the Author

*[Susheel Varma](https://susheelvarma.com) is Chief Data Officer at [Sage Bionetworks](https://sagebionetworks.org) and was previously Chief Technology Officer at [Health Data Research UK](https://hdruk.ac.uk/), where he co-authored the TRE Green Paper and Building Trusted Research Environments guidance. The protocol-level arguments are vendor-neutral by design and not endorsed by any one organisation.*

*This post refers to: Emrys Health and Nesta (2025/2026). Health Data Research Service (HDRS) Digital Ecosystem Analysis, Final Report. Wellcome Open Research.*

*For the companion reading guide, see [What Wellcome Found When It Audited the UK's Health Data Infrastructure](https://opentre.org/blog-hdrs-reading-guide.html). For the technology guarantee argument, see [The Technology Guarantee](https://opentre.org/blog-hdrs-technology-guarantee.html).*

---

Copyright 2026 Susheel Varma. Licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
