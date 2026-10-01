# Computational Analysis of Wellbeing-Related Language

An independent exploratory study investigating computational approaches to characterize emotional expression, affective markers, and social support signals in public natural language data.

## Research Objectives
- Evaluate the extent to which surface-level lexical representations capture nuanced emotional and wellbeing-related states.
- Establish a rigorous, reproducible evaluation baseline using public social media discourse.
- Identify failure modes and boundary limitations of linear n-gram baselines when applied to conversational, multi-label text.

## Current Project Status
- **Status:** Exploratory data analysis and baseline classification completed.
- **Dataset:** GoEmotions (Google Research), curated under the Apache License 2.0.

| Stage | Milestone | Status |
|---|---|---|
| 1 | Dataset selection, licensing, and ethical risk review | Completed |
| 2 | Exploratory data analysis & token frequency distribution | Completed |
| 3 | Multi-label baseline modeling (TF-IDF + Logistic Regression) | Completed |
| 4 | Quantitative per-label evaluation (Macro/Micro F1) & error analysis | Completed |

## Repository Structure
- `notebooks/01_exploratory_analysis.ipynb`: Data inspection, token length dynamics, label distributions, and frequency analysis.
- `notebooks/02_baseline_and_error_analysis.ipynb`: TF-IDF vectorization, multi-label Logistic Regression classifier, per-label metrics, and error examination.
- `DATASET_PLAN.md`: Dataset rationale, provenance, privacy bounds, and ethical governance considerations.
- `requirements.txt`: Environment dependencies.

## Key Observations & Limitations
1. **Class Disparity:** Frequent categories (e.g., *admiration*, *approval*) achieve high recall, while subtle negative states (e.g., *remorse*, *grief*) face severe data sparsity challenges.
2. **Contextual Invariance:** Bag-of-words representations struggle with negation, conversational sarcasm, and implicit affect.
3. **Ethical Bounds:** This repository models textual annotations in public discourse; it does not infer individual psychological diagnoses or clinical mental health states.

## Future Direction
- Benchmark against pretrained transformer representations (e.g., RoBERTa / DeBERTa) to capture contextual dependencies and subtle emotional nuances.
