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

Bayesian Networks are a statistical modelling technique that represents the joint probability between variables. Mixed networks allow modelling of discrete and continuous variables but require that continuous variables are Gaussian and have linear relationships. Neither of which can be guaranteed when performing exploratory modelling. However, despite this restriction the technique can be used for exploratory modelling to gain insight into the data. Later, in modelling the data, any potential non-Gaussian and non-linearity in the data can be accounted for by adding additional variables to the Bayesian Network (Gaussian Mixture Models are great for this).

The Titanic dataset is used to showcase the use of Bayesian Networks to focus Exploratory Data Analysis (EDA) on key data features to speed up the analysis. An added bonus is that a Bayesian Network can be trained on data that contain missing values.
