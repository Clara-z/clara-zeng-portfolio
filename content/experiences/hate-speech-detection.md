---
title: "Hate Speech Detection Project"
date: 2023-12-01
draft: false
tags: ["BERT", "NLP", "Machine Learning", "Deep Learning"]
---

## Overview

Built and compared machine learning models for automated hate speech detection on social media, implementing both traditional ML approaches and state-of-the-art transformer models.

## Problem Statement

Hate speech on social media platforms:

- Harms targeted individuals and communities
- Spreads rapidly and is difficult to moderate manually
- Requires automated detection at scale
- Needs nuanced understanding of context and language

## Dataset

Worked with a dataset of **40,000+ social media text samples** containing:

- Hate speech examples
- Offensive but non-hateful content
- Neutral content

The multi-class nature of the problem required careful handling of class boundaries and imbalanced distributions.

## Approach

### Model 1: TF-IDF + Naive Bayes (Baseline)

Implemented a traditional ML pipeline:

1. **Text Preprocessing**
   - Tokenization
   - Stop word removal
   - Lemmatization
   
2. **Feature Extraction**
   - TF-IDF vectorization
   - N-gram features (unigrams and bigrams)

3. **Classification**
   - Multinomial Naive Bayes classifier
   - Fast training and inference
   - Interpretable feature importance

### Model 2: Fine-tuned BERT (Advanced)

Implemented a transformer-based approach:

1. **Pre-trained Model**
   - BERT base model
   - Pre-trained on large text corpora

2. **Fine-tuning Strategy**
   - Task-specific classification head
   - Learning rate scheduling
   - Early stopping to prevent overfitting

3. **Optimization**
   - Weights & Biases hyperparameter sweep
   - Systematic search over learning rates, batch sizes, epochs

## Hyperparameter Optimization

Used **Weights & Biases** for:

- Automated hyperparameter sweeps
- Experiment tracking and comparison
- Visualization of training metrics
- Model version control

### Key Hyperparameters Tuned

| Parameter | Search Range | Optimal Value |
|-----------|--------------|---------------|
| Learning Rate | 1e-5 to 5e-5 | 2e-5 |
| Batch Size | 16, 32 | 32 |
| Epochs | 3-5 | 4 |
| Warmup Steps | 0-500 | 100 |

## Results

### Performance Comparison

| Model | Test Accuracy | F1 Score |
|-------|---------------|----------|
| Naive Bayes | 72.3% | 0.69 |
| **BERT (Fine-tuned)** | **79.5%** | **0.77** |

### Key Findings

- BERT significantly outperformed traditional ML approaches
- Early stopping was crucial to prevent overfitting
- Class imbalance required careful handling through weighted loss

## Error Analysis

Conducted comprehensive error analysis revealing:

- **False Positives:** Often triggered by offensive-but-not-hateful content
- **False Negatives:** Missed subtle or coded hate speech
- **Challenging Cases:** Sarcasm, context-dependent meaning

### Documented Limitations

- Difficulty with emerging slang and coded language
- Context window limitations
- Potential bias in training data

## Research Paper

Documented all findings in a full research paper covering:

- Literature review
- Methodology
- Experimental results
- Error analysis
- Future work recommendations

## Skills Applied

- BERT (Language Model)
- Naive Bayes Classification
- Hyperparameter Optimization
- Natural Language Processing
- Experiment Tracking (W&B)
- Research Writing