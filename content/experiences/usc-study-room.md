---
title: "USC Study Room Rating Web Application"
date: 2022-12-01
draft: false
tags: ["React.js", "Java", "MySQL", "Full-Stack"]
---

## Overview

Built a full-stack web application serving **5,000+ USC students** to crowdsource ratings and reviews for **100+ campus study locations**. The platform helps students find the perfect study spot based on community feedback.

## Problem Statement

USC students faced challenges finding good study spaces:

- Information about study locations was scattered
- No centralized platform for reviews and ratings
- Difficult to know which spaces were quiet, had outlets, or were crowded
- No way to reserve spaces in advance

## Solution

### Crowdsourced Study Space Reviews

Created a platform where students can:

- **Rate study locations** on multiple criteria
- **Write detailed reviews** about their experiences
- **View aggregate ratings** to make informed decisions
- **Filter and sort** locations based on preferences

### Rating Criteria

Students rate each location on:

- Noise level (quiet to loud)
- Availability of power outlets
- WiFi quality
- Seating comfort
- Crowdedness at different times
- Natural lighting

## Features

### Search, Sort, and Filter

Implemented comprehensive search functionality:

- **Search by name** - Find specific buildings or rooms
- **Sort by rating** - See top-rated spaces first
- **Filter by amenities** - Outlets, WiFi, quiet zones
- **Filter by location** - Near specific buildings or areas

### Reservation System

Built a reservation feature allowing students to:

- Book study rooms in advance
- View availability calendars
- Receive confirmation notifications
- Cancel or modify reservations

### User Profiles

- Track personal review history
- Save favorite study spots
- Build reputation through helpful reviews

## Technical Architecture

### Frontend

- **React.js** - Modern, responsive UI
- **Component-based design** - Reusable UI elements
- **Real-time updates** - Live rating changes

### Backend

- **Java** - Robust server-side logic
- **RESTful APIs** - Clean interface between frontend and backend
- **Authentication** - Secure user accounts

### Database

- **MySQL** - Relational database for structured data
- **Efficient queries** - Optimized for search and filtering
- **Data integrity** - Proper constraints and relationships

### API Design

```
GET    /api/locations         - List all study spaces
GET    /api/locations/:id     - Get specific location details
POST   /api/locations/:id/reviews - Submit a review
GET    /api/locations/search  - Search with filters
POST   /api/reservations      - Create a reservation
```

## Impact

### User Adoption

- **5,000+ active users** among USC student body
- **100+ locations** catalogued and reviewed
- Reduced time students spend searching for study spaces

### Community Value

- Centralized scattered information into one platform
- Enabled data-driven decisions about where to study
- Created a sense of community around shared experiences

## Skills Applied

- Full-Stack Development
- React.js
- Java
- MySQL
- REST API Design
- User Experience Design
- Database Modeling