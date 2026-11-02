
---
title: 'Dealing with SonarQube Cloud: Initial Results from a Mining Software Repository Study'
authors:
- Sabato Nocera
- Davide Fucci
- Giuseppe Scanniello
date: '2025-09-01'
publishDate: '2025-09-01T09:10:02.380498Z'
publication_types:
- paper-conference 
publication: 'Proceedings of the 19th ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM25)'
url_pdf: https://arxiv.org/pdf/2508.18816
abstract: >-
  Background: Static Code Analysis (SCA) tools are widely adopted to enforce code quality standards.
  However, little is known about how open-source projects use and customize these tools. Aims: This
  paper investigates how GitHub projects use and customize a popular SCA tool, namely SonarQube
  Cloud. Method: We conducted a mining study of GitHub projects that are linked through GitHub
  Actions to SonarQube Cloud projects. Results: Among 321 GitHub projects using SonarQube Cloud, 81%
  of them are correctly connected to SonarQube Cloud projects, while others exhibit
  misconfigurations or restricted access. Among 265 accessible SonarQube Cloud projects, 75% use the
  organization's default quality gate, i.e., a set of conditions that deployed source code must meet
  to pass automated checks. While 55% of the projects use the built-in quality gate provided by
  SonarQube Cloud, 45% of them customize their quality gate with different conditions. Overall, the
  most common quality conditions align with SonarQube Cloud's "Clean as You Code" principle and
  enforce security, maintainability, reliability, coverage, and a few duplicates on newly added or
  modified source code. Conclusions: Many projects rely on predefined configurations, yet a
  significant portion customize their configurations to meet specific quality goals. Building on our
  initial results, we envision a future research agenda linking quality gate configurations to actual
  software outcomes (e.g., improvement of software security). This would enable evidence-based
  recommendations for configuring SCA tools like SonarQube Cloud in various contexts.
---
