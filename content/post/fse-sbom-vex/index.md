---
title: First project publication at FSE25
date: 2025-03-21 
authors: [Davide Fucci]
image:
  caption: ""
  focal_point: "Top"
  preview_only: false
---

_"Augmenting Software Bills of Materials with Software Vulnerability Description: A Preliminary Study on GitHub"_ is the first papar published in the context of the SESAM project and covering an important aspect of software security-software supply chain. 

Software Bill of Materials (SBOMs) have become a key asset in ensuring transparency and trust in the software supply chain.
As regulations like the U.S. Executive Order 14028 and the European Union's Cyber Resilience Act come into force, both private and public organizations are required to disclose the components of their software and manage associated risks.

Despite their growing importance, current SBOMs are often limited to listing dependencies without offering insight into whether those dependencies introduce vulnerabilities. This gap significantly undermines the utility of SBOMs in security risk assessment.

### Exploring SBOM Augmentation with VEX
To address this limitation, our team conducted a preliminary study investigating the value of augmenting SBOMs with vulnerability information using the **Vulnerability Exploitability eXchange (VEX)** format. VEX provides a structured way to communicate whether known vulnerabilities in software components are exploitable in the context of a given project.

We analyzed 40 open-source GitHub repositories using the CycloneDX SBOM format. After identifying known vulnerabilities (CVEs) in their dependencies using osv-scanner, we generated corresponding VEX files. These files added contextual data to the SBOMs, helping consumers understand the exploitability of listed vulnerabilities.

We submitted pull requests (PRs) to each project, including the VEX files and a short survey to gather maintainer feedback. Over a 60-day observation period, we tracked responses, comments, and decisions related to the PRs.

### Key Findings
- **VEX adds value**: Maintainers acknowledged that enriched SBOMs offer improved visibility into potential security risks.
- **Automation is essential**: A recurring theme was the need for automated and continuous updates of SBOMs and VEX data, ideally as part of CI/CD workflows.
- **Standardization is lacking**: Some maintainers expressed reluctance to adopt VEX due to limited support and evolving standards.
- **Existing tools are insufficient**: While tools like Dependabot and Grype are widely used, they lack features for structured lifecycle tracking of vulnerabilities, which VEX provides.

### Implications for the Open Source Ecosystem 
The study highlights a clear opportunity to improve the practical utility of SBOMs in open-source projects. By integrating VEX data, maintainers can offer users and auditors deeper assurance about the security posture of their software.

However, adoption hinges on lowering the barrier to entry. Tooling must evolve to make VEX generation seamless and integrated with development pipelines. Moreover, industry-wide consensus on formats and best practices will be crucial to facilitate widespread adoption.

### Looking Ahead: SBOM and VEX in the SESAM Project
This vision paper is just the beginning. Within SESAM we will explore how SBOM are used by developers in one of our industry partner to support security activities, such as code reviews, and what is the role of VEX for commercial software products to align with emerging regolatory frameworks.

📍 We’ll present our work at the **ACM Foundations of Software Engineering (FSE) '25** conference in Trondheim, Norway. 

📄 The preprint is available [here](https://arxiv.org/abs/2503.13998) while the dataset and replication material is on the project GitHub [repository](https://github.com/SESAM-project/SBOM-VEX-acceptance).



