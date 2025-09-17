---
title: "Beyond just a list of dependencies: what policy‑driven SBOMs reveal"
date: 2025-09-17
authors: [Davide Fucci]
image:
  caption: ""
  focal_point: "Top"
  preview_only: false
---

SBOMs are central to software supply‑chain transparency and are referenced by emerging regulations (e.g., U.S. EO 14028, EU CRA).
Once these regulations are enforced, developers (both in open source and industrial projects) and software companies will have to deal with this new artifact, integrate it into their workflows, and share it with downstream customers. Yet little is known about SBOMs created to meet security and compliance policies in practice—as opposed to synthetic or test artifacts.
Our latest work, published at the International Conference on Product-Focused Software Process Improvement (PROFES 2025), examines those _policy‑driven_ SBOMs at scale.

# The study 
[Previously]({{< relref "fucci-2025-augmenting" >}}), we analyzed SBOM from GitHub in conjunction with VEX to understand how open source maintainers will deal with them.
Now, we turned our attention to _policy-driven_ SBOMs. These are SBOM that serve a real policy, such as compliance or vulnerability management, rather than, for example, being generated for testing purposes, or as the basis to develop new tools for parsing SBOM in research settings.
To identify policy-driven SBOMs, we created a series of heuristics based on their contents, the analysis of the repositories containing them, and other properties.
 We mined 26,823 GitHub repositories, identified 620 policy‑driven SBOM files (SPDX and CycloneDX), and evaluated (i) their structure and quality, (ii) vulnerability exposure across 28 advisory databases.

# What we found 
We confirm that adoption is low: only 0.56% of processed repositories contained a policy‑driven SBOM. Among these, Golang projects were most represented.
There are quite divided camps when it comes to formats, 336 SBOM files used SPDX, and 284 CycloneDX. On the bright side, JSON dominates over representations such as XML and YAML.
Nevertheless, most SBOMs do not use the latest spec versions (e.g., SPDX 3.0 is unused).

There is a significant variation in the quantity of information these SBOMs contain. Across SBOMs, there are 181,283 dependencies (25,430 unique) with a heavy‑tailed distribution.
Their quality also varies, but they mostly reach a sufficient (6+/10) level.

Looking at vulnerabilities in the reported dependencies, we found 19,225 CVE occurrences (2,202 unique, whereas a good amount of dependencies (39.15%) had no known vulnerabilities.
Interestingly, the most common class of vulnerability is CWE‑20 (input validation), with DoS categories (CWE‑400/1333/770) also prominent.

Finally, we observed 384 unique licenses, although one in every five reported dependencies in an SBOM does not report license information. Apache‑2.0 and MIT are the most used licenses for approximately 70% of occurrences in our dataset.

# What does that mean for you
If you are an open source maintainer or software supplier, upgrade to current formats to avoid future compatibility gaps (e.g., when it comes to attestations).
For security teams, consider that when present, SBOMs reveal non‑trivial medium/high‑severity exposure in the dependencies they document. It would make sense to document such vulnerabilities better by integrating SBOM with VEX. [A discussed previously]({{< relref "fucci-2025-augmenting" >}}), this can help communicate exploitability and prioritize remediation in line with time‑bound obligations (e.g., the one imposed by EU CRA).
Finally, to facilitate the job of legal and compliance teams, the variety of downstream licenses and frequent missing license data argue for automated SBOM‑driven license checks early in the pipeline.

# Where do we go from here?
We plan to study the time dimension (when SBOMs appear, how specs evolve) and maintainer-specific policies for creating and maintaining SBOMs, validating the policies we based this study on.

[Our dataset](https://github.com/AleX04Nov/sbom_scanning) of 620 policy‑driven SBOMs with quality and vulnerability annotations is provided for replication and further research.

