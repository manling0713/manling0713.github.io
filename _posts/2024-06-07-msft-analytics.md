---
layout: post
title: "Microsoft Sales Performance Analytics"
subtitle: "Leveraging CRM Data and ML to optimize Microsoft Enablement Programs"
tags: [Python]
categories: [projects]
image: "/assets/img/msft.avif"
full-width: true
---

## 💡 Business Problem
#### 1. Do Enablement Programs drive an Increase in revenue?
- What variables affect revenue?
- What is the nature of the relationship, and how can we use this information to improve upskilling initiatives?
#### 2. Which targeted subsets of product consumption are impacted differently?
- Who are the different customer segments and what are their characteristics?
- How can we cater upskilling courses to these segments to maximize product consumption?

## 📊 Dataset
The dataset was anonymized and comprised 19 columns with over 516,000 rows.  
Data Overview:
![fig1](/assets/img/msft1.png)

## 🛠️ Tools
- Tools: Python
- Skills: Data Aggregation, XGBoost, K-Prototypes Clustering

## 🔬 Methodology
#### 1. Data Cleaning
- Missing values: Missing values were simply dropped because some customers included either class or spend information due to the different time scopes of the data.
- Data Aggregation: Combined some raw data rows based on customer and month. For example, instead of including every course number a customer took, we aggregated them to represent the number of courses the customer took in that month.

#### 2. XGBoost
**Business Goals**  
- Assessed the impact of participation in enablement programs on revenue across different customer segments.
- Identified critical features and their specific roles in influencing revenue to optimize resource allocation and strategy development.

**Business Implications**   
a. Target Role: Training employees in specific roles, particularly Roles B and C, is crucial as it directly correlates with a substantial increase in revenue.

![fig2](/assets/img/msft2.png)

b. Product Category: Increased sales in key product categories such as meat and fruits are strongly correlated with spikes in revenue, highlighting the potential for targeted marketing and sales initiatives to amplify growth in these crucial product categories.

![fig3](/assets/img/msft3.png)

### 3. K-Prototypes

**Business Goals**  
- Target Marketing: Enables Microsoft to tailor products or services more precisely to specific customer segments, thereby increasing sales efficiency and engagement.
- Resource Allocation: Allocate more resources to customers who potentially generate more revenue to increase conversion rates from customer acquisition to higher revenue.

![fig4](/assets/img/msft4.png)

**Recommendations & Strategies**  
- **Cluster 1 (Exploratory Users):** Develop customized learning paths; offer trial/discounts.  
- **Cluster 2 (Moderate Contributors):** Develop content for industry-specific challenges; build referral programs.  
- **Cluster 3 (High-Value Investors):** Offer VIP coaching and highly personalized programs.  
- **Cluster 4 (Diverse Leaders):** Customized courses for Role A, C & M; build specialized online engagement forums.


## 🎯 Conclusions
1. Enablement participation strongly correlates with increased spending; key factors: roles (B, C, E) and industries (Serpentine, Peridot).  
2. Identified 4 customer segments differing in spend and engagement.  
3. Recommendations by customer size:  
   - Small: Build awareness of upskilling opportunities.  
   - Medium: Develop relationships to increase engagement.  
   - Large: Deepen relationships to drive revenue.

## Links
<a href="https://github.com/manling0713/Microsoft-Enable-Program" class="btn btn-primary" target="_blank">
  Github Repo
</a>
