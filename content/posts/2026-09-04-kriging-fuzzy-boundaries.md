---
title: Kriging with Fuzzy Domain Boundaries
subtitle: The Idea that was shelved for 14 years
date: 2026-09-04
draft: false
repositories:
  - "Mining-Ds-Vault"
  - "Mining-Ds-Toolkit"
tags:
  - "Research"
  - "Kriging"
  - "Fuzzy Boundaries"
  - "Go"
# Vault-specific links
target_doc: "/reports/research/kriging-fuzzy-boundaries.pdf"
target_source: https://github.com/matthew-nimmo/mining-ds-vault/tree/main/research/Kriging-Fuzzy-Boundaries
---

In 2012, standard resource estimation offered only two choices at domain boundaries: hard cut-offs (zero samples outside) or soft buffers (all samples inside treated as 100% equal). When I proposed scaling sample weights continuously based on domain membership, the traditional consensus was sceptical. Fourteen years later, with the rise of non-stationary spatial kernels, inverse-variance penalties, and machine-learning spatial proxies, the mathematics has caught up. Here is the formal proof why discrete fuzzy domain membership works.
