---
title: Exploratory Modelling with Bayesian Networks
subtitle: Kaggle Titanic - Machine Learning from Disaster dataset
date: 2026-05-27
draft: false
repositories:
  - "Mining-Ds-Vault"
tags:
  - "Discover"
  - "Bayesian Networks"
  - "Data Analysis"
  - "Titanic Dataset"
  - "R"
# Vault-specific links
target_doc: "/reports/discover/titanic-data-analysis.pdf"
target_source: https://github.com/matthew-nimmo/mining-ds-vault/tree/main/discover/Titanic-Data-Analysis
---

Most people who work with the Titanic dataset follow the same path: load the data, engineer a few features, and train a random forest to predict survival. It’s a good exercise. But it skips the most important part of the analysis.

Understanding the data.

For this example, I use the Titanic dataset as a statistical storytelling problem, not a machine-learning (ML) competition. The goal isn’t to build the most accurate model. It is to uncover the relationships that explain why certain groups survived and others didn’t.

It’s a practical example of how Bayesian Networks can be used for exploratory analysis in real mining datasets. To understand structure and reveal dependencies before building any predictive model.

Bayesian Networks are one of my favourite statistical modelling techniques. I use it a lot to gain an understanding of geometallurgical data. I even use it to build an initial model of the complete data, not just selected variables (features), and to help discover what data is missing. Knowing what data we don't have is just as important as knowing what data we do have. The confounder can really hurt an analysis and the modelling. 

Using Bayesian Networks, we can:
- learn the conditional dependencies between variables
- visualise the structure of the data as a directed acyclic graph
- identify which variables influence survival directly or indirectly
- query the model to answer questions like:
 “Given age, class, and sex, what is the probability of survival?”
- generate synthetic passengers to test hypotheses
- combine latent variables with a Bayes‑style classifier to estimate survivability
- perform ML counter-factual analysis

I did this analysis several years ago. I have made some structural edits and moved it inside the mining-ds-vault where the full source code (R and Quarto report) can be viewed.
