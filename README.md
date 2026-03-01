# Defensible Inferences from a Nested Sequence of Logistic Regressions

This repository contains the replication code and statistical methodology for the peer-reviewed article:  
**"Defensible inferences from a nested sequence of logistic regressions: a guide for the perplexed"** *Authors: Gulsah Gurkan, Yoav Benjamini, and Henry Braun* *Published in: Large-scale Assessments in Education (2021)*

[**Read the Full Open-Access Paper Here**](https://link.springer.com/article/10.1186/s40536-021-00111-7)

---

## 📌 Project Overview
In social science and policy research, researchers often use a **nested sequence of models** to explore how "mediators" (like education or skills) account for the impact of a "predictor" (like family background) on an "outcome" (like income). 

However, in **logistic regression**, adding variables to a model changes the scale of the coefficients. This makes direct comparisons between nested models statistically biased, which is a phenomenon known as the **rescaling problem**.

This project provides a robust solution by:
1.  Implementing a modified **Karlson–Holm–Breen (KHB) method** to obtain unbiased estimates of mediation effects.
2.  Applying the **Benjamini-Hochberg (BH) procedure** to control the **False Discovery Rate (FDR)** across hierarchically structured hypotheses (across 20+ countries).

---

## 📊 Data Source & Research Design
The methodology is demonstrated using data from the **OECD’s Programme for the International Assessment of Adult Competencies (PIAAC)**.

* **Objective:** Analyzing how educational attainment and measured cognitive skills (literacy/numeracy) mediate the relationship between socio-economic background and the probability of being a low-wage earner (bottom 25% of the national income distribution).
* **Sample:** Full-time employees across multiple participating countries.
* **Technical Challenge:** Handling complex survey weights and plausible values within a nested logistic framework.

---

## 💻 Methodology
The analysis is implemented in **R**. Key technical features include:

* **Bias Correction:** Using the KHB method to ensure that changes in coefficients across models reflect true mediation rather than scaling artifacts.
* **Multiplicity Control:** Managing the increased risk of Type I errors when testing similar hypotheses across dozens of countries using FDR-adjusted p-values.
* **Reproducibility:** Scripts are designed to handle Large-Scale Assessment (LSA) data structures efficiently.

---

## 📖 Citation

If you utilize this methodology, the modified KHB implementation, or the replication scripts, please cite the peer-reviewed article:

> Gurkan, G., Benjamini, Y., & Braun, H. (2021). Defensible inferences from a nested sequence of logistic regressions: a guide for the perplexed. *Large-scale Assessments in Education*, 9(16). https://doi.org/10.1186/s40536-021-00111-7
