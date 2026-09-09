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

They’re the most powerful tool we have to stop fooling ourselves with historical data. In geometallurgy and mining data science, the biggest risks aren’t bad assays or noisy test‑work. It’s the hidden structural bias we introduce without realising it. And once it’s baked into a model, the damage is done.

The challenge:

Across geology, metallurgy, and mining analytics, selection bias creeps in quietly.

I’ve seen it first-hand. Two labs, two rounds of metallurgy test‑work, and a big discrepancy. At first glance, Lab B looked wrong, Until the DAG revealed the real culprit. Different rock properties sent to each lab. The “lab bias” wasn’t a lab bias at all. It was a hidden selection variable.

This pattern repeats everywhere:
• Filtering out “bad” samples without causal justification.
• Rejecting outliers because they “look wrong”.
• Using domains as if they were geological truths (when they’re actually colliders).
• Mistaking correlation for causation, especially when ML elevates proxy variables like trace elements.

Each of these creates structural bias. Each distorts the model. And each leads teams to confidently walk into a statistical trap.

The solution:

We can’t eliminate all bias, but we can prevent most of the self‑inflicted ones.

Two steps matter more than any model code:

1. Treat data analysis like product development.
Write a Business Understanding document or PRD that defines decisions, boundaries, semantics, and failure modes. Align the team before a single line of code is written.

2. Use Directed Acyclic Graphs (DAGs).
A DAG is the explicit contract for meaning. It shows what causes what, which paths are open or closed, and where selection variables or colliders sit. It prevents semantic traps between geologists, metallurgists, and data scientists. It reveals miss‑specification before the model does.

A simple DAG can prevent months of wasted effort and millions in downstream operational mistakes.

The next challenge:

It’s using them.

The real missing link in mining data science the absence of shared, open‑source causal DAGs that describe known geological and metallurgical relationships. Because at the end of the day:

Same rock properties (G) + same operational conditions (M) = same metallurgical response (R).

And when we separate universal physical causality (G → M → R) from project‑specific constraints (P), we unlock modular, scalable DAGs that work anywhere in the world.

DAGs become product infrastructure. They can be versioned, governed, shared, and reused. When we treat them like products, they become the structural rails that keep analytics, modelling, and AI aligned with reality and reduce the risk of data analytics projects failing because of cognitive bias or the semantic trap.
