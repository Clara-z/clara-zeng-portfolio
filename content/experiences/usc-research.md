---
title: "Research Assistant at USC"
date: 2024-01-01
draft: false
company: "University of Southern California"
role: "Research Assistant"
duration: "Jan 2024 - May 2025"
location: "Los Angeles, California"
tags: ["Privacy-Preserving ML", "Knowledge Distillation", "LLMs", "Differential Privacy"]
---

## Overview

As a Research Assistant at USC, I conducted cutting-edge research on privacy-preserving techniques for large language models. My work focused on enabling the benefits of powerful LLMs while protecting sensitive training data.

## Research Focus: Privacy-Preserving Knowledge Distillation

### The Problem

Large language models like GPT-2 are trained on massive datasets that may contain sensitive information. When deploying these models or sharing them, there's a risk of inadvertently leaking private data from the training set.

### My Approach

I researched **privacy-preserving knowledge distillation** — a technique that transfers knowledge from a large "teacher" model to a smaller "student" model while incorporating privacy guarantees.

Key components of my research:

#### Model Alignment

Aligned attention and hidden layers between:
- **Teacher Model:** GPT-2
- **Student Model:** DistilGPT2

This alignment ensures the student model learns meaningful representations from the teacher while being more compact and efficient.

#### Differential Privacy Integration

Integrated **Differentially Private Stochastic Gradient Descent (DP-SGD)** into the training process. This provides mathematical guarantees about privacy:
- Bounds the influence any single training example can have
- Adds calibrated noise to gradients during training
- Enables quantifiable privacy budgets (ε, δ)

### Results

The approach enhances data confidentiality **without significant loss in model performance**, making it practical for real-world deployment where privacy is a concern.

## Framework Re-engineering

In addition to the core research, I:

- **Re-engineered** a text dataset distillation framework using Hugging Face models
- **Redesigned data-loading pipelines** for efficiency and compatibility
- **Initiated full algorithm reimplementation** to enable seamless integration with differential privacy mechanisms

## Publications & Presentations

*Research ongoing - details to be updated upon publication*

## Skills & Technologies

- **Models:** GPT-2, DistilGPT2, Hugging Face Transformers
- **Privacy:** Differential Privacy, DP-SGD, Privacy Accounting
- **Techniques:** Knowledge Distillation, Layer Alignment
- **Tools:** PyTorch, Hugging Face, Opacus