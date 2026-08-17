# Internship Retrospective: Engineering Real-World ML Pipelines

**Target Audience:** Ziad Khalil (Week 1 Self)  
**Track:** Machine Learning & AI Engineering Pipeline  

---

## 1. What I Set Out to Do vs. What Changed

When I started in Week 1, my perspective on machine learning was heavily centered around model selection and tuning. I viewed the core challenge as finding the highest-performing algorithm for traffic decay detection. 

However, as the weeks progressed—specifically during the DuckDB feature pipeline implementation and feature leakage audits in Weeks 3–6—my engineering priorities shifted completely. I realized that 80% of real-world ML failure modes stem from subtle data contract violations, temporal leakage, and flawed baseline logic rather than model architecture limitations. Instead of jumping straight to complex time-series models, I pivoted toward building a clean feature pipeline and establishing clear data boundary contracts using a Random Forest classifier as a transparent baseline.

---

## 2. What I Would Build Next

If I were extending this project into a production system, I would focus on three key upgrades:

1. **Live Search Console API Integration:** Replacing synthetic proxy data with direct webhooks pulling real-time GSC impression and click data.
2. **Dynamic Decay Thresholds:** Transitioning from the fixed 35% drop ratio to standard deviation-based relative thresholds that account for seasonal search volume fluctuations.
3. **Automated MLOps Pipeline:** Integrating n8n or GitHub Actions to run the DuckDB feature pipeline weekly and trigger auto-refresh queues when content decay is detected.

---

## 3. Top 3 Transferable Engineering Skills Learned

1. **Feature Leakage Prevention & Data Contracts:** Learning how to rigorously test features for temporal leakage (preventing future information from bleeding into training data) using SQL/DuckDB logic before passing matrices to Scikit-Learn.
2. **Iterative Baseline Modeling:** Developing a habit of shipping simple, verifiable baselines first, evaluating metrics like F1-score transparently, and justifying every incremental hyperparameter change.
3. **AI Transparency Diligence:** Utilizing AI tools (Gemini / Claude) productively as logic soundboards while maintaining strict personal accountability over edge-case handling, data integrity, and domain verification.

---

## Conclusion to Week 1 Ziad

Focus on the data contracts and data quality before the algorithms. The value of an ML engineer lies in identifying system constraints, testing for data leaks, and clearly documenting real-world limitations—not just delivering high validation scores on clean benchmark datasets.
