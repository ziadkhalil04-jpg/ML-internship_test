# FlyRank Search Content Decay Detection & ML Pipeline

## Overview
This repository contains the end-to-end Machine Learning pipeline designed for **FlyRank** to detect search performance decay across published content before traffic drops severely. By comparing 90-day baseline impression volume with 30-day evaluation windows, this system identifies pages requiring immediate updates.

## System Architecture
```text
# ML Internship Capstone Project

## Architecture & Data Flow

```text
[ Raw Impression Data ] ──► [ Exclusion Rules (Baseline >= 10) ] ──► [ Feature Engineering ]
                                                                             │
[ Automated Refresh Queue ] ◄── [ Random Forest Classification ] ◄──────────┘
```

---

## Quick Start Guide (For Reviewers & External Developers)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ziadkhalil04-jpg/ML-internship_test.git
   cd ML-internship_test
   ```

2. **Install dependencies:**
   ```bash
   pip install numpy pandas scikit-learn matplotlib
   ```

3. **Run the Capstone Notebook:**
   Open `work/notebooks/capstone.ipynb` in Jupyter Notebook, VS Code, or Google Colab and run all cells sequentially.

---

## Evaluation Results (v2 Model)

* **Model:** Random Forest Classifier (Optimized)
* **Metric:** F1-Score ~ 0.82 on validation split
* **Top Predictors:** `baseline_impressions` and `content_age_days`

---

## Model Limitations

* **Synthetic Proxy Data:** The evaluation uses simulated metrics representing public-safe traffic patterns; live production deployment requires connection to Search Console APIs.
* **Static Threshold:** Decay is classified on a fixed 35% drop ratio, which may not capture seasonal fluctuation without secondary time-series features.

---

## AI Transparency Diligence

* **AI Assistance Statement:** This codebase and research paper were built using Gemini / Claude as an AI thinking partner for drafting boilerplate and baseline logic. All domain configurations, feature leakage checks, data contracts, and final code reviews were independently conducted and validated manually by Ziad Khalil.

---

## Internship Index

| Week / Task | Module Name | Deliverable Link |
| :--- | :--- | :--- |
| **Week 1-2** | ML Task Framing & Data Contracts | [w01_research_question.ipynb](https://github.com/ziadkhalil04-jpg/ML-internship_test/blob/main/work/notebooks/w01_research_question.ipynb) |
| **Week 3-4** | Feature Leakage & DuckDB Pipeline | [w03_feature_leakage_check.ipynb](https://github.com/ziadkhalil04-jpg/ML-internship_test/blob/main/work/notebooks/w03_feature_leakage_check.ipynb) |
| **Week 5-6** | Baseline Model & Refinement | [w05_baseline_model.ipynb](https://github.com/ziadkhalil04-jpg/ML-internship_test/blob/main/work/notebooks/w05_baseline_model.ipynb) |
| **Week 7-8** | Capstone Research Paper | [capstone.ipynb](https://github.com/ziadkhalil04-jpg/ML-internship_test/blob/main/work/notebooks/capstone.ipynb) |
| **FL-09** | Documentation & AI Transparency | [README.md](https://github.com/ziadkhalil04-jpg/ML-internship_test/blob/main/README.md) |
| **FL-10** | Internship Retrospective | [retrospective.md](https://github.com/ziadkhalil04-jpg/ML-internship_test/blob/main/docs/retrospective.md) |
