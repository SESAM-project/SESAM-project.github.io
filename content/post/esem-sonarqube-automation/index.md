---
title: Starting to uncover automation configurations for security
date: 2025-08-27
authors: [Davide Fucci]
image:
    caption: ""
    focal_point: "Top"
    preview_only: false
---

Understanding automation in software security policies is one of the focal points of the **SESAM** project—**SEcure software engineering through _Sensible AutoMation_**. 

Our team began examining how automation is configured in open-source projects on GitHub. Specifically, we looked at the effort developers put into configuring tools that serve a security purpose, such as static code analyzers. 
The broader goal is to compare these practices with what large software organizations do, such as Ericsson that is part of the project consortium, and to compile guidelines for _sensible_ automation configurations—deciding when static policies are sufficient and when more dynamic, adaptive approaches might be needed.

### The study
Our recent study, published in the New Ideas and Emerging Results track at the Empirical Software Engineering and Measurement (ESEM25) conference, is titled **“Dealing with SonarQube Cloud: Initial Results from a Mining Software Repository Study.”**
We analyzed 265 active, popular GitHub projects connected to SonarQube Cloud via GitHub Actions.

### Key Findings
We found that 75% of the projects relied on the organization's default quality gate.
Of these, 55% used SonarQube's built‑in "Sonar way" while only 45% customized their gates.
Interstingly, the built‑in quality gate conditions for security appeared in 91% of projects

### Next Steps
Together with the industry partners of the project, we have few next steps lined up.
1. **Investigate why developers customize quality gates.** We are currently planning a more qualitative study to explore motivations and contexts.
2. **Develop adaptive quality gates.** Leveraging AI-based approaches to create dynamic configurations to better reflect project and stakeholders needs.
3. **Study integrations with other SCA tools.** As it is common to use multiple code analyzer tools, such as [CodeScene](https://codescene.com), their interaction poses interesting research direction (e.g., on aligning dynamic configurations to accommodate combined toolchains).
4. **Link configurations to outcomes.** At a more fundamental level, empirical evidence connecting tool configuration policies to software outcomes (such as reduced vulnerabilities or improved maintainability) is necessary to guide sensible automation practices.

The pre-print of the paper is available on [arXiv](https://arxiv.org/abs/2508.18816).

