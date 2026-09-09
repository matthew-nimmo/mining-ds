---
title: Scoring Functions
subtitle: Validating Twin Drill Holes for Resource Estimation
date: 2026-06-17
draft: false
repositories:
  - "Mining-Ds-Vault"
tags:
  - "Discover"
  - "Data-Profiling"
  - "Scoring"
  - "R"
# Vault-specific links
target_doc: "/reports/discover/scoring-functions_twin-dh.pdf"
target_source: https://github.com/matthew-nimmo/mining-ds-vault/tree/main/discover/Scoring-Functions
---

Geological data validation can include the use of twin drill holes to verify the repeatability of mineralization and identify spatial variability. Traditionally, assessing these pairs involves subjective visual inspections of scatter plots and downhole logs, a process that does not scale across large databases. This notebook introduces the foundational concept of Scoring Functions as a mechanism to quantify data integrity. By translating physical geological variance into a normalized, deterministic metric, we demonstrate how raw assay deviations can be mapped to a standardized quality KPI. Using a synthetic copper, iron, and sulphur dataset, we provide a reproducible R framework for modular data assessment, bridging the gap between traditional geological quality control and scalable data engineering.
