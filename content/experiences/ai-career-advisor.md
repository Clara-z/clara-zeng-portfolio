---
title: "AI-Based Career Advisor"
date: 2025-05-01
draft: false
tags: ["LLMs", "Python", "Streamlit", "NLP"]
---

## Overview

Designed and developed an interactive AI-based tool to help users plan and explore career paths by leveraging their skills and interests. The application provides real-time, actionable recommendations with direct links to learning resources.

## Problem Statement

Career planning is challenging, especially for students and early-career professionals who:

- Don't know which career paths align with their skills
- Struggle to identify skill gaps for target roles
- Need personalized guidance but can't afford career coaches
- Want actionable next steps, not generic advice

## Solution

### Interactive Career Planning Tool

Built a **Streamlit-based UI** that allows users to:

1. Input their current skills and interests
2. Explore matching career paths
3. Identify skill gaps for target roles
4. Get personalized learning resource recommendations

### Large Language Model Integration

Utilized multiple LLM technologies:

- **GPT APIs** - For natural language understanding and personalized recommendations
- **Llama3** - For efficient, cost-effective inference on certain tasks

### Massive Dataset Integration

Leveraged **1.3 million dataset entries** from:

- **O*NET** - Comprehensive occupational database with skill requirements
- **LinkedIn** - Real-world job posting data and career trajectories

## Key Features

### Real-Time Skill Gap Analysis

The system compares user skills against target role requirements to identify:

- Skills the user already possesses
- Critical gaps that need to be addressed
- Nice-to-have skills for competitive advantage

### Personalized Learning Resources

For each identified skill gap, the tool provides:

- Specific online courses and tutorials
- Recommended certifications
- Hands-on project ideas
- Direct links to resources

### Career Path Exploration

Users can explore:

- Multiple career paths matching their profile
- Salary ranges and job market demand
- Typical career progression timelines
- Related roles they might not have considered

## Technical Stack

- **Frontend:** Streamlit
- **Backend:** Python
- **LLMs:** GPT APIs, Llama3
- **Data Sources:** O*NET, LinkedIn (1.3M entries)
- **NLP:** Natural Language Processing for skill extraction and matching

## Impact

The tool democratizes career guidance by providing personalized, data-driven recommendations that were previously only available through expensive career coaching services.