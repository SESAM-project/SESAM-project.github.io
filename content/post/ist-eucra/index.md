---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Preparing for the EU Cyber Resilience Act: what are companies doing today?"
subtitle: ""
summary: ""
authors: [Davide Fucci]
tags: [research]
categories: []
date: 2026-09-24T17:43:13+02:00
lastmod: 2026-09-24T17:43:13+02:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---


The EU Cyber Resilience Act (CRA) is changing what companies need to demonstrate about the security of their products. Secure development, vulnerability handling, software supply-chain transparency, and technical documentation are all central concerns. Reporting obligations for actively exploited vulnerabilities and severe security incidents have applied since 11 September 2026; the main obligations apply from 11 December 2027. [European Commission](https://digital-strategy.ec.europa.eu/en/policies/cyber-resilience-act)

But how are companies preparing in practice?

In our latest SESAM study, **“Preparing for the EU Cyber Resilience Act: A Study with Four Swedish Companies,”** accepted in *Information and Software Technology*, we investigated this question with practitioners from the Swedish software industry.

## The study

We interviewed nine practitioners from four Swedish companies, two large enterprises and two SMEs. The interviews took place in spring 2025 and covered security, development, verification, architecture, and technical-leadership roles.

We examined current security practices, EU CRA interpretation, compliance planning, evidence artefacts, and organisational challenges. Our analysis considered both the security work participants described and their companies’ preparedness to demonstrate conformity through defined processes, ownership, and traceable evidence.

One important distinction emerged. **Doing security work is not necessarily the same as being able to demonstrate that the work was done.**

## Security practices exist, with different levels of formalisation

Across the cases, the participants described activities relevant to the EU CRA, including secure code review, vulnerability tracking, static analysis, security release documentation, and dependency-update policies. Their organisation and degree of formalisation varied considerably.

One large enterprise, connected product-security ownership, supply-chain control, release-linked component registration, and a dedicated post-release vulnerability-management system. The other was integrating emerging product-cybersecurity routines into existing safety, quality, and verification structures, with uneven visibility across roles.

The SMEs also differed. One embedded security into a small group of engineers with multiple roles, supported by documented workflows, dependency checks, pull-request reviews, and responsible disclosure routines; meanwhile the other relied more on informal developer knowledge and reactive security work.

What seems to matter is **institutionalisation** of security work becoming part of stable processes, clear responsibilities, and traceable artefacts. A large organisation can still face fragmented responsibilities, while an SME can establish a comparatively strong foundation through disciplined everyday engineering.

## Two ways of handling vulnerabilities in everyday development

For vulnerability handling, one area strongly emphasized by EU CRA, we show a contrast between the two SMEs. Both connect vulnerability handling to development, but with different structures.

In one company, security triage, mitigation investigation, review, and a quality gate make the handling of a vulnerability explicit. A small team coordinates through pull requests and automated dependency gates. Security-related issues still share a development process with feature work and bugs, but priority is what distinguishes them.
This differentiation becomes largely indistinguishable from ordinary bug fixing in the other SME.

For practitioners, the useful question is whether a vulnerability remains recognisable throughout the workflow, who owns it, how it is assessed, what remediation decision is made, and which records preserve that decision. Integration into normal development can be efficient, but security-relevant work must remain visible and traceable.

## SBOMs are part of the picture

Software Bills of Materials (SBOMs) also featured in the interviews. One large enterpreise described an established release-level component inventory and SBOM process. Other cases relied more on dependency reports, manifests, package lists, and other SBOM-like artefacts. None of the cases demonstrated a fully standardised end-to-end workflow.

The gap was therefore often in turning existing component information into a stable, reusable artefact that could be communicated externally. Similarly, release records, tickets, code reviews, and analysis results could support compliance, but companies did not always recognise or maintain them as evidence.

This connects with our earlier SESAM work on [policy-driven SBOMs](https://sesam-project.github.io/post/profes-policydriven-sbom/), which examines SBOMs used for vulnerability management or licence compliance.

## What this means for sensible automation

The study identifies an opportunity for tools to reduce the effort of producing reusable compliance evidence from existing development work. Tools could collect dependency information from manifests and CI/CD pipelines, generate and update SBOMs, connect vulnerabilities to releases and components, and package the resulting information for reuse.

We also call for support for vulnerability intake, triage, disclosure, and distinguishing security issues from ordinary defects. These are implications for tool providers, rather than automation benefits evaluated by this study.

## Five practical takeaways

1. **Build on existing processes.** Connect security, supplier, release, and compliance work, with explicit ownership and evidence responsibilities across teams.
2. **Keep SME workflows lightweight and repeatable.** Integrate security into existing development without needing to reproduce a large enterprise’s organisational structure.
3. **Make vulnerabilities visible and traceable.** Where practices are reactive, establish responsibility for vulnerability handling and distinguish vulnerability reports from functional defects through intake channels and issue categories.
4. **Turn development artefacts into reusable evidence.** Tool providers should reduce the operational effort of maintaining component inventories and compliance documentation, alongside finding vulnerabilities.
5. **Translate obligations into workable routines.** Regulators should accompany requirements with practical guidance that fits engineering work, especially in SMEs.

**Read the paper:** Oleksii Novikov, Davide Fucci, Daniel Mendez, and Oleksandr Adamov. *Preparing for the EU Cyber Resilience Act: A Study with Four Swedish Companies.* Information and Software Technology (2026). [DOI: 10.1016/j.infsof.2026.108321](https://doi.org/10.1016/j.infsof.2026.108321).
