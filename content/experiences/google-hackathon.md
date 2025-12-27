---
title: "Customer Churn Diagnosis – Google x Berkeley Analytics Hackathon"
date: 2024-12-01
draft: false
tags: ["Business Analytics", "Python", "Statistical Analysis", "Data Storytelling"]
---

## Overview

**Top 3 Finalist** in the Google x UC Berkeley Analytics Hackathon. Diagnosed a 3x customer churn spike for a SaaS company by analyzing messy, real-world datasets and delivered an executive-ready recommendation projected to retain $23M in annual contract value.

## Problem Statement

BizGrow, a SaaS inventory management platform, saw churn spike from 4% to 12% in one quarter. Leadership was divided:

- Sales blamed product performance
- Product blamed low-quality customer acquisition
- Support felt overwhelmed by tickets

The COO needed one actionable recommendation with limited resources—not a dashboard or 50 charts.

## Solution

### Reframing the Problem

Defined churn by **revenue impact** rather than customer count. Enterprise contracts were 46x more valuable than SMBs, so logo-based churn metrics obscured the real risk.

### Root Cause Analysis

Analyzed three datasets with real-world flaws (missing values, corrupted EU server logs, unstructured text):

- **CRM Data** – Contract dates, company size, industry (~30% missing)
- **Usage Logs** – Daily login activity (EU September data corrupted)
- **Support Tickets** – Unstructured customer complaints

## Key Findings

### Customer Success > Technical Failures

- **58% of churned customer tickets** were customer success issues (onboarding friction, sales expectation gaps)—not product bugs
- Customers with only CS-related tickets churned at **21.5%** vs **14.9%** for technical-only tickets

### Small Companies Drive Volume, Not Value

- Small companies (1-10 employees) drove **75% of churn** but represented only 34% of customers
- Revenue impact was concentrated in enterprise accounts

### Usage Drops Signal Frustration

- Session time dropped significantly on ticket-filing days (p=0.017)
- Validated that complaints reflected real user friction, not noise

## Recommendation

The fastest lever: close the **expectation gap** between what sales promised and what customers experienced.

- Retrain sales on accurate product positioning
- Implement structured onboarding check-ins for first 60 days
- Proactively monitor low-usage customers as churn indicators

**Projected Impact:** Retain ~$23M ACV and reduce daily support load by 193 hours.

## Technical Stack

- **Analysis:** Python, pandas, scipy
- **Methods:** Statistical significance testing, ticket text classification, cross-dataset validation
- **Deliverable:** Executive slide deck with data-driven narrative

## Impact

Demonstrated ability to navigate ambiguous business problems, handle messy data, and translate analysis into actionable recommendations under time pressure—core skills for data science in business contexts.