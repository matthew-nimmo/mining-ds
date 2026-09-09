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

In the early 2000 when I was first doing Mineral Resource estimation I followed the rule book. I processed the geological data in the standard way, dealing with outliers using the typical clip at a threshold method (98th percentile being common). I happily built complex 3D wireframe models of the geology. And I did spatial estimation using Ordinary Kriging.

In 2006 it struck me that doing Ordinary Kriging or any form of kriging was compute expensive. The problem was matrix inversion. This was being done for every sample estimate. I surmised that their must be a way to minimize the cost of the matrix inversion. I started playing with Kalman Filters.

In 2012 (and earlier) I surmised that rather than updating the weights, what if there was a way to augment the kriging matrices in such a way that when including a sample it can be switched on or off and the corresponding weights will be equivalent to the kringing weights if the sample was in or out. This lead to the idea of kriging with fuzzy domain boundaries.

That work stopped in 2012.

Fourteen years later, I have continued that work. From the fragments of legacy work came a more complete experiment. Now there are three variants that I have tested and have corresponding implementations in Go. The mechanism I proposed in 2012 to deal with hard and soft boundaries also offers a path for dramatically reducing the runtime of Sequential Gaussian Simulations (SGS).

Go implementation benchmarks:

Ordinary Kriging ~553 ns/op, 19 allocs/op
Variant A: ~570 ns/op, 19 allocs/op (full matrix inversion)
Variant B: ~558 ns/op, 19 allocs/op (full matrix inversion)
Variant C: 11.68 ns/op, 1 allocs/op (recursive matrix update)

Variant C leverages recursive updates to deliver a ~47x speedup, potentially turning multi-hour SGS runs on million-node block models into sub-minute computations.

There is still a lot of work to be done to build a production ready solution but the work so far is very encouraging.
