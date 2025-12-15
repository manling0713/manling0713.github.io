---
layout: post
title: "Fetch: Offer Like These"
subtitle: "Optimizing offer strategies with ML and AI Insights"
tags: [SQL, Python, Snowflake, GPT API, Streamlit]
categories: [projects]
image: "/assets/img/fetch.png"
full-width: true
---

⚠️ The screenshot of this project might be unclear or partially hidden due to confidential information, but feel free to reach out if you’d like to discuss it further.

## ℹ️ Background

### What is [Fetch](https://fetch.com/)?
Fetch is an app that lets you earn rewards by scanning your shopping receipts, turning everyday purchases into points redeemable for gift cards.

### What is [Fetch Offer](https://fetch.com/blog/fetch-tips-tricks/what-is-an-offer-on-fetch)?
Fetch offers are special deals on select products or retailers that give you extra points when you buy and scan those items’ receipts.

DoorDash Offer Example:  

<img src="/assets/img/fetch1.png" alt="DoorDash Offer Example" height="600">

## 💡 Business Problem

When creating new offers, sales teams often rely on past offers as references. For example, to design an offer for Coca-Cola, they might look at previous offers made for Pepsi.
- What factors should we use to define offers as similar?
- How can a tool help optimize the offer creation strategy and improve key performance metrics, such as Return on Ad Spend (ROAS), for our partners?

![fig2](/assets/img/fetch2.png)

## 📊 Dataset
The dataset includes all offers executed in the past 2 years.

**Offer Attributes:** Points awarded, Spend (Cost), Target Buyer, Offer Duration, Other relevant features
**Performance Metrics:** Redemptions, Redemption Rate, Return on Ad Spend (ROAS), Incremental ROAS (iROAS), Additional KPIs

![fig3](/assets/img/fetch3.png)

## 🛠️ Tools
- Tools: SQL, Python, Snowflake, GPT API, Streamlit
- Skills: Machine Learning, AI Analysis(GPT-4)

## 🔬 Methodology
### 1. Data Cleaning  
Missing Values: Addressed by collaborating with Sales and the Analytics Engineer teams, leveraging business acumen to establish a cutoff threshold—only offers with more than 100 redemptions were included in the database.
    
### 2. Models Overview
- Voyager: I implemented a machine learning model called [Voyager](https://spotify.github.io/voyager/), developed by Spotify, to identify similar offers within our dataset. Voyager is a Python library designed for approximate nearest-neighbor (ANN) search, enabling efficient similarity matching across high-dimensional data.
- AI Analysis: Integrated the GPT-4 model to provide clear explanations of why offers are considered similar and recommend potential strategies for optimization.
- Defined business-relevant similarity criteria, requiring offers to share the same category, tactic, and target audience.
- Applied a simple scoring method to further prioritize offers from the same partner, with barcode overlaps, and belonging to the same sub-category.

![fig4](/assets/img/fetch4.png)

### 3. How to use the tools?

The app is an interactive Streamlit app designed for Sales and non-technical stakeholders. Users can input an offer_id, and the app will retrieve the top 3 most similar offers. A large language model (LLM) then generates an analysis and strategic recommendations. Additionally, users can enter their own questions into a built-in chatbot to request further explanations or insights.

![fig5](/assets/img/fetch5.png)
![fig6](/assets/img/fetch6.png)
![fig7](/assets/img/fetch7.png)

## 🎯 Conclusions
This tool combines a machine learning model with AI-powered analysis to help the Sales team create offers more efficiently, eliminating the need to manually search for similar offers in our platform. It also bridges the gap between the Data team, Sales, and GTM, enabling them to leverage data-driven insights to better meet the Sales team’s business needs.
