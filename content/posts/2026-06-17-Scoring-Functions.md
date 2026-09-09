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

Geological data validation can include the use of twin drill holes to verify historic drill hole data, verify high-grade assay intersections, and check for sampling bias. Traditionally, assessing these paired data involves subjective visual inspections of scatter plots, quantile-quantile plots, and down-hole logs, or the use of global statistics—a process that does not scale across large databases.

To overcome the problem of scaling the analysis, Scoring Functions are introduced to illustrate how the observed geological variability between the paired data can be translated into a normalized, deterministic metric, which can then be used as a standardized quality KPI.

A simple synthetic dataset containing two drill holes treated as a twin pair—with lithology and assays for copper, iron, and sulphur—is used to demonstrate the mechanics under the hood.

The example notebook added to my mining-ds-vault GitHub repository forms a reproducible R framework for modular data assessment, bridging the gap between traditional geological quality control and scalable data engineering.

🩺 𝐃𝐞-𝐑𝐢𝐬𝐤𝐢𝐧𝐠 𝐭𝐡𝐞 𝐃𝐞𝐩𝐨𝐬𝐢𝐭: 𝐓𝐡𝐞 𝐃𝐚𝐭𝐚 𝐇𝐞𝐚𝐥𝐭𝐡 𝐂𝐡𝐞𝐜𝐤

The cell-based scoring function is just one component of a comprehensive data auditing framework I deploy to run health checks on Geological and Geometallurgical data before resource estimation or predictive modelling.

I focus entirely on back-end analytics and spatial modelling to deliver a rigorous, engineered diagnostic report covering:

- Data Profiling: Describing the data and exposing hidden problems before data preparation even begins.

- Data Quality Scoring: Quantifying data quality and building metrics for use in machine learning, spatial modelling, and benchmarking.

- Data Gap Analysis: Quantifying exactly what critical geological and geometallurgical data is missing.

The framework systematically explores both "what you have" and "what you don't have" in your data asset.
