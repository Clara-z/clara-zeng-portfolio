---
title: "Data Analyst Intern at Bluebono"
date: 2025-08-01
draft: false
company: "Bluebono"
role: "Data Analyst Intern"
duration: "Jun – Aug 2025"
location: "Los Angeles, California"
tags: ["Real Estate Analytics", "Data Engineering", "Python", "Machine Learning", "Feature Engineering"]
---

## Overview

During my Data Analyst internship at Bluebono, I worked on a residential real estate analytics project connecting local housing market conditions to loan-to-value (LTV) decision-making.

The core insight: property risk is not only about the property itself. A similar home can carry different lending risk depending on whether it sits in a liquid, competitive ZIP code or a slower market with rising inventory and longer days on market. My work focused on turning that local market context into a cleaner, more interpretable signal.

---

## What I Built

An end-to-end data pipeline for ZIP-level residential property evaluation. The pipeline pulled together large-scale housing market data, cleaned and validated it, engineered market indicators, and fed a scoring framework that adjusts LTV recommendations by local market strength.

The project touched both data science and software engineering:

- **Data scale:** 11.3M+ raw property and market records across 1,000+ California ZIP codes, with history from ~2012 through 2025
- **Market indicators studied:** median sale price, price per square foot, homes sold, pending sales, new listings, inventory, days on market, sale-to-list ratio, off-market velocity
- **Engineering:** API-based property data ingestion via Trestle/CoreLogic, comparable-property matching logic

The goal was not a black-box valuation model — it was a defensible framework that could explain why one local market supports a higher LTV cap while another should be treated more conservatively.

---

## Pipeline Details

**Data preparation** was the first challenge. Real estate data arrived in multiple formats: monthly market files, property records, percentage fields, price strings, dates, and region identifiers. I wrote cleaning logic to normalize columns, convert prices and percentages to numeric values, align monthly time periods, and filter to relevant California markets.

**Feature engineering** focused on signals that describe market strength from several angles:

| Dimension | Features |
|---|---|
| Price movement | Median sale price, price/sqft, YoY change |
| Liquidity | Homes sold, pending sales, inventory, new listings |
| Market speed | Median days on market |
| Buyer competition | Sale-to-list ratio, homes sold above list, off-market velocity |
| Stability | Volatility and longer-term trend behavior |

**Dimensionality reduction:** I applied unsupervised clustering to group correlated variables, reducing redundant market features by ~65%. Many real estate variables tell overlapping stories — sale price, list price, price/sqft, and YoY price movement are related but shouldn't all over-count the same signal.

**Scoring layer:** I combined a transparent rule-based baseline (easy to explain to stakeholders) with a gradient-boosted model to capture nonlinear relationships. Feature-importance analysis translated the model back into business-readable drivers.

**Comparable-property matching:** I prototyped logic for matching a subject property to relevant comps using address similarity, geographic distance, property size, lot size, sale date, price, and listing status — connecting the ZIP-level market score to the practical workflow of evaluating a specific property.

---

## Results

- Transformed messy provider data into structured, interpretable market features
- Reduced feature complexity by ~65% through clustering
- Created a dynamic LTV framework: instead of treating every property market the same, the system explains why stronger, more liquid markets support more confidence while volatile markets warrant conservative lending assumptions
- Built reusable components for market data cleaning, API-based ingestion, feature preparation, and comp filtering

---

## Key Design Decisions

**Market-level risk modeling.** The most important choice was modeling risk at the ZIP-code level, not just the individual property. Valuation tells you what an asset may be worth today, but LTV risk also depends on how resilient that value is — a liquid, high-demand market is easier to exit than one with rising inventory and slow sales.

**Respecting time.** Housing data is naturally time-series data. A random train-test split would let future market behavior leak into the past. Time-based train/validation/test splits better matched the real question: given only historical data up to this point, how well can we score the next period?

**Conservative missing data handling.** Short gaps in monthly indicators can be filled from nearby months since these metrics move gradually. Long gaps at the start or end of a ZIP's history are different — filling those aggressively creates false confidence, so I treated them carefully and avoided future information in validation periods.

**Interpretability over complexity.** In a lending-adjacent workflow, a score is only useful if stakeholders understand what drives it. Combining a rule-based baseline with ML-assisted discovery let the model reveal nonlinear patterns while keeping the final explanation grounded in business logic.
