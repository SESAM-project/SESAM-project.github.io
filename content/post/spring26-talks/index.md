---
title: "Two industry talks from the SESAM project: GenAI, supply chains, and sensible automation"
authors: [Davide Fucci]
date: 2026-04-28
image:
---

In March and April, the SESAM project had the opportunity to present ongoing work to two industry audiences: first at SIEMENS (Munich, Germany) on March 30, and then at Sony (Lund, Sweden) on April 21.

The two talks approached the SESAM project goal of integrating security into software engineering practices without overwhelming developers or creating counter-productive automation from different but connected angles: GenAI security, shift-left security, and software supply-chain resilience.

## GenAI security and shift-left security

The March 30 talk, online with 20 SIEMENS security experts, focused on the security implications of GenAI and on SESAM’s work around shifting security activities earlier in the development lifecycle.
The first part, presented by Oleksandr Adamov, who is also part of the [SEAM team]({{< relref "people/index.md" >}}) discussed how AI is changing the threat landscape. AI can be used as a weapon, attacked as a target, or embedded into applications in ways that create new risks. The talk covered AI-assisted cyber operations, LLM-related threats, OWASP Top 10 risks for LLM applications, and the need to rethink how we secure AI-enabled software systems.

The second part of the talk connected to SESAM’s broader focus on shift-left security. The main message was that automation is necessary, but not sufficient. Static analysis, GUI testing, dependency review, SBOMs, CI/CD checks, and policy-as-code can all help, but only if they are configured and interpreted sensibly. Otherwise, automation risks becoming noise rather than support.  ￼

This is exactly the kind of problem SESAM is meant to address: how to integrate security into development practices while avoiding automation that creates extra work, unclear responsibility, or misplaced confidence. SESAM’s previous work on [SonarQube configurations]({{< relref "post/esem-sonarqube-automation" >}}), for example, has already shown that many projects rely heavily on default or built-in security gates, raising questions about when fixed policies are enough and when more adaptive policies are needed.

## Breaking the software supply chain

The April 21 talk at the headquarter of Sony Sweden in Lund with a mix of security experts and software developers was titled , _“Breaking the chain: Building resiliency against software supply-chain attacks,”_ and focused on another core SESAM theme: securing the modern software supply chain.

The talk started from a simple observation: modern software is assembled, not written from scratch. Source code, package registries, build systems, containers, deployment environments, cloud infrastructure, and third-party dependencies all become part of the final product. This makes development faster, but also creates many entry points for attackers.

The presentation covered concrete attack patterns such as typosquatting, malicious packages, compromised maintainers, stolen publishing tokens, and attacks on build systems. The point was not only that these attacks exist, but that supply-chain security requires visibility across many layers of the development and release process.

A major part of the talk focused on SBOMs and VEX. SBOMs can provide visibility into the components of a software product, but not all SBOMs serve the same purpose. Design, source, build, analyzed, deployed, and runtime SBOMs answer different questions and support different use cases, including vulnerability management, licensing, and regulatory compliance.

This connects directly to SESAM’s research on [policy-driven SBOMs]({{< relref "post/profes-policydriven-sbom" >}}) and [vulnerability information]({{< relref "post/fse-sbom-vex" >}}). SESAM work has highlighted that SBOMs are useful, but often incomplete if they only list dependencies. Integrating vulnerability information through VEX can help communicate exploitability and support remediation decisions, especially in the context of time-bound obligations such as those introduced by the EU Cyber Resilience Act.

The final part of the April talk discussed the EU Cyber Resilience Act and how companies are preparing for it. The slides addressed product security, vulnerability disclosure, open-source implications, and the need for maturity models that help organizations assess where they stand.

## What we took away for SESAM

Across both talks, one common message emerged: security is becoming more integrated into software engineering, but also more complex.

GenAI introduces new kinds of systems and new kinds of threats. Supply-chain attacks exploit the dependencies and infrastructure that modern development relies on. Regulations such as the EU CRA increase the need for evidence, traceability, and clear responsibility. At the same time, developers cannot be expected to manually absorb all of this complexity.

That is where SESAM focus on sensible automation becomes important. The goal is not to automate everything. The goal is to understand what should be automated, what should remain under human control, and how tools can provide useful, explainable support instead of simply adding more alerts and dashboards.

Thanks to SIEMENS and Sony for the invitations and for the constructive discussions. These exchanges with industry are essential this project and its sustainability as they help us keep the research grounded in real development challenges and ensure that our results remain useful beyond academic prototypes.
