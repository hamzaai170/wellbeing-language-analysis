# Dataset Plan

This document records which public dataset the project uses, why, and how ethical and licensing questions are handled.

## Selection Criteria

1. Publicly available with a clear, permissive license for research use.
2. Text already de-identified or anonymized by the dataset authors.
3. Labels relevant to emotional expression or social support.
4. Well documented, with a published paper describing how it was built.
5. Small enough to run on a standard workstation or free Colab environment.

## Primary Dataset: GoEmotions

- **What it is:** Approximately 58,000 English Reddit comments, annotated by human raters across 27 emotion categories plus neutral.
- **Source:** Demszky et al. (2020), *GoEmotions: A Dataset of Fine-Grained Emotions*, ACL 2020, released by Google Research.
- **Access:** Hugging Face `google-research-datasets/go_emotions` (simplified configuration used in exploratory analysis).
- **Why it fits:** Emotion labels provide a structured baseline proxy for affective language in online communities, supported by extensive documentation and benchmark literature.
- **Known limits:** Informal Reddit comments only, English language only, short text lengths, subjective annotator boundaries, and indirect representation of interpersonal family/relationship dynamics.
- **License:** Apache License 2.0 (Permissive open-source research license).

## Data Handling and Ethics

- **Boundary Enforcement:** Only the officially released dataset is utilized. No supplementary web scraping or profile querying is conducted.
- **Privacy & Anonymization:** No attempt is made to re-identify, de-anonymize, or contact any post author. Any username or metadata artifact is discarded prior to modeling.
- **Repository Cleanliness:** Raw data files are excluded from git tracking. Data pipelines fetch directly from verified upstream endpoints.
- **Reporting Restraint:** Exemplar texts displayed in notebooks are minimal and strictly illustrative. No private or sensitive disclosures are reproduced.
- **Non-Clinical Scope:** Analytical outputs characterize aggregate corpus patterns. No diagnostic claim or individual psychological inference is made.

## Decisions Log

| Date | Decision | Note |
|---|---|---|
| October 2026 | Selected GoEmotions as primary baseline dataset | Verified Apache License 2.0 on Google Research / Hugging Face repository |
| October 2026 | Implemented TF-IDF + Logistic Regression benchmark | Established multi-label baseline and documented error patterns |