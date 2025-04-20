---
title: Recommendation System (Part 1)
date: 2025-04-19 22:18:00 
categories: [Study notes]
tags: [recommendation_system]
math: true
comments: true
---

### 1. Introduction to Recommendation Systems

There are many ways to describe recommendation systems.

For me, I like to sum it up in one sentence:  
**“If you’re here, you’re staying — one scroll leads to another.”**  
Think of TikTok, Instagram... the more you scroll, the more addicted you get.

Recommendation systems are everywhere:
- “You may like this” or “You might be interested in that” — sound familiar?
- The bigger the company, the smarter the recommendation system.
- Everyone sees different content — it's personalized for each user.
- What you do determines what gets recommended to you.

---

### 2. Why Do We Need Recommendation Systems?

- Only a few products are truly popular — but what about everything else?
- Around **80% of sales come from 20% of the products**.
- To increase overall revenue, we need to promote **long-tail items**.
- Personalized recommendations based on user behavior help push those lesser-known products.

{% include custom-image.html src="assets/img/2025-4-20-Study-notes/2025-4-20-study-notes-1.png" width="400" alt="" %}

---

### 3. Goals of a Recommendation System

A good recommendation system isn’t just about pushing content — it’s about pushing the *right* content:

- **Relevance**: The content must be related to the user’s interests.
- **Novelty**: Recommending something new keeps users engaged.
- **Serendipity**: Sometimes the best recommendations are unexpected — like finding a hidden gem.
- **Diversity**: Variety is important — users don’t want to see the same kind of thing over and over.

{% include custom-image.html src="assets/img/2025-4-20-Study-notes/2025-4-20-study-notes-2.png" width="400" alt="" %}

---

### 4. Common Terminology in Recommendation Systems

- **Item**: A product, video, article — whatever is being recommended.
- **Embedding**: A hidden vector representation of items or users (e.g., from matrix factorization).
- **Recall**: The stage of roughly filtering down to a smaller set of possible recommendations.
- **Scoring**: Ranking those items with a common metric.
- **Re-ranking**: Adjusting the final order based on finer details or business rules.

---

### 5. Typical Recommendation Pipeline

Most recommendation systems work in three stages: **Offline + Nearline + Online**  
And in three phases: **Recall → Rough Ranking → Fine Ranking**

- **Offline**: Trains big models on historical data. It’s updated periodically.
- **Rough ranking (nearline)**: Updates recommendations based on user actions in near real-time.
- **Online (final stage)**: Applies business rules and gives the final ranked list instantly when the user is active.

---

### 6. Challenges in Building Recommendation Systems

- Requires deep understanding of users: collecting rich profile and behavior data.
- People change — interests evolve over time.
- Recommendations should evolve too — they can’t stay static.
- Feature engineering is complex and ever-changing.
- Cold start problems:
  - **New user**: We don’t know their preferences yet.
  - **New item**: No one has interacted with it before.
- It’s easier to handle new items — they have fixed attributes.
- Solutions:
  - Use content-based filtering
  - Use hybrid models
  - Collect implicit signals as early as possible

---

### 7. Deep Learning in Recommendation Systems

**Why use deep learning?**

- **Big Picture**: Manual feature engineering is hard — deep learning automates and improves it.
- **Core Advantage**: End-to-end models simplify the process and improve performance.
- **Best Fit**: Works especially well for NLP and image-based content, which is common in user behavior data today.

---
