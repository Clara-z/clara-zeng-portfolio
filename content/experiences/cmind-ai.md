---
title: "Associate Data Scientist at Cmind AI"
date: 2025-12-01
draft: false
company: "Cmind AI"
role: "Associate Data Scientist"
duration: "May 2024 – Dec 2025"
location: "Remote"
tags: ["Machine Learning", "MLOps", "Financial ML", "NLP", "LLMs", "Python", "MLflow", "XGBoost"]
---

### Overview

As an Associate Data Scientist at Cmind AI, I worked on AI systems that supported **earnings prediction and financial text analysis**. The work combined data science, software engineering, MLOps, and analyst-facing product thinking — the goal was not only to train accurate models, but to build workflows that could ingest financial data, generate predictions, explain signals, and support recurring analysis.

Cmind publishes regular earnings prediction and market-analysis updates, so the technical work had to fit a real business rhythm: new financial data arrived continuously, earnings calendars changed, and analysts needed outputs that were reproducible, interpretable, and useful for decision-making.

---

### Building End-to-End Prodcution Pipeline

One of my main contributions was improving the **EPS surprise prediction workflow** — predicting whether a company would beat or miss consensus EPS expectations using historical financial, market, sector, and macroeconomic features.

I refactored the workflow into modular Python components for data loading, feature construction, model training, evaluation, prediction, and experiment tracking. Instead of treating the model as a one-off notebook, the pipeline became closer to a production ML workflow where each step had a clear responsibility.

This software engineering work mattered because financial ML changes often. A team may want to compare new models, adjust features, change validation strategy, or rerun predictions for a new reporting period. Modular design made those changes faster and safer.

---

### Modeling Financial Data

For the core tabular prediction task, I worked primarily with **XGBoost** and benchmark-style model experimentation. XGBoost was a practical choice because the data was structured, sector-level sample sizes were limited, and tree-based models perform well on nonlinear interactions between financial ratios, prior performance, estimates, and macro variables.

The most important modeling lesson was that financial prediction is **time-sensitive** — a model should only learn from information available before the earnings event being predicted. I focused on time-aware feature engineering, including shifted quarterly features and change-based signals, to capture both a company's current state and the direction its fundamentals were moving.

I also addressed class imbalance and high-dimensional features, using imbalance-handling strategies, feature selection, and validation metrics that better reflected the real prediction task. In targeted quarterly runs, the system achieved **~90% forecast accuracy** in selected evaluation settings.

---

### MLOps and Reproducibility with MLflow

A major part of the project was making experiments reproducible. I integrated **MLflow** to track model parameters, metrics, artifacts, and model versions — allowing the team to compare experiments, understand which choices produced each result, and manage models more systematically.

For engineers, MLflow reduced ambiguity around model versions and experiment history. For analysts, reproducibility increased trust: a prediction was the output of a traceable workflow, not just a number.

I also learned to think beyond headline metrics. Accuracy, F1, AUC, and precision on high-confidence predictions answer different questions. For an analyst-facing product, the most valuable metric is often how reliable the **top-ranked opportunities** are, not overall accuracy.

---

### Financial NLP and LLM-Based Analysis

Alongside structured EPS prediction, I worked on **earnings-call transcript analysis** — a signal source that financial statements alone may not capture: management confidence, evasiveness, tone, and forward-looking commentary.

I helped build a transcript analysis workflow combining **FinBERT** with **OpenAI API** calls:

- **FinBERT** handled scalable domain-specific sentiment scoring
- **LLM prompts** supported contextual tasks: speaker role extraction, paragraph attribution, evasiveness scoring, and bullishness/bearishness explanations

The result was a workflow that turned messy transcript text into organized, analyst-ready tables for downstream analytics.

---

### Data and Deployment Integration

The project also required connecting models to real data sources and operational workflows. I worked with integrations across **Oracle Cloud, AWS S3, MongoDB**, and analytical storage — not just as infrastructure details, but as the layer that determined whether models could be used repeatedly in a business setting.

A strong model is not useful if the data is hard to retrieve, outputs are difficult to inspect, or the process cannot be rerun reliably. I focused on workflows that could support both analyst review and production-style data movement.

---

### Results and Impact

- **EPS prediction system** became more modular, maintainable, and easier to iterate on
- **MLflow integration** made model experiments and versioning transparent across the team
- **Transcript analysis pipeline** added explainable NLP signals from earnings calls
- **Cloud integrations** connected research workflows to practical, analyst-facing analytics.
