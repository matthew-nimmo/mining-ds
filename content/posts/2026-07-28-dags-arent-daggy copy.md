---
title: DAGs aren’t daggy
subtitle: Directed Acyclic Graphs for data analytics in the Mining Industry
date: 2026-07-28
draft: false
repositories:
  - "Mining-Ds-Vault"
tags:
  - "Discover"
  - "Geometallurgy"
  - "DAG"
  - "R"
# Vault-specific links
target_doc: "/reports/discover/dag.pdf"
target_source: https://github.com/matthew-nimmo/mining-ds-vault/tree/main/discover/DAG
---

DAGs aren’t daggy—they’re the only reliable way to stop fooling ourselves with historical data. As a geometallurgist or data scientist, it’s dangerously easy to introduce hidden selection variables by filtering or comparing data without understanding the causal structure.

A simple lab‑A versus lab‑B discrepancy might look like bad test‑work, but a DAG reveals the real culprit: different rock properties driving different outcomes. Filtering out samples, rejecting outliers, or comparing operators without considering geology can quietly distort the dataset and lead to biased models, flawed interpretations, and costly operational mistakes. Strong correlations can also be misread as causes when key variables—like lithology—were never measured.

Time and again, the trap is the same: we had the data, we ran the model, and everything made sense until we realised we never checked the DAG. So what is a DAG?
