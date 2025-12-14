---
layout: post
title: "Behavioral Analytics and CLV Insights with IBM Watson Marketing"
subtitle: "Customer lifetime value modeling & renewal strategy insights"
tags: [Python, R]
categories: [projects]
image: "/assets/img/ibm.avif"
full-width: true
---

## 💡 Business Problem

### 1. New Customer Acquisition
- Which customers are the most valuable (CLV) and how do we identify prospects that will be valuable customers?
- The aim is to identify the most valuable customers in terms of Customer Lifetime Value (CLV). The objective is to develop strategies for new customer acquisition by identifying and targeting individuals with high potential CLV. We will analyze customer demographics, behaviors, and other relevant factors.
### 2. Renewal and Churn Prevention
- How do we drive policy renewals? What renewal marketing efforts are working?
- The goal is to improve the rate of policy renewals and identify effective marketing efforts. This will involve analysis of customer satisfaction, customer experience, marketing campaigns, incentives, and other communication channels.

## 📊 Dataset

The dataset comprises 24 columns, including 2 metrics designed for customer performance evaluation and 22 variables associated with customer data.
Data Source: IBM Official Website

## 🛠️ Tools
- Tools: R Studio (glm), Python (pandas, NumPy, seaborn, and matplotlib)
- Skills: Semi-Log Regression Model, Logistic Regression

## 🔬 Methodology
### 1. Exploratory Data Analysis (EDA)

a. CLV Distribution: The median CLV is around $7,000, while the mean CLV is approximately $10,000, indicating a right-skewed distribution. This skewness suggests a significant portion of customers have a CLV below the average, with over 80% of customers having a CLV under $10,000.

![fig1](/assets/img/ibm1.png)
![fig2](/assets/img/ibm2.png)

b. Response Rate vs. Employment Status:The tallest bar is for "Employed" indicating it has the highest count of positive responses, while the shortest bars are for "Disabled" and "Medical Leave", indicating the lowest counts of positive responses. The bars for "Retired" and "Unemployed" are of similar height, indicating similar counts of positive responses for these categories.

![fig3](/assets/img/ibm3.png)

### 2. Data Modeling and Analysis
    
a. Semi-Log Model:
- Customer Lifetime Value follows a skewed distribution, with a few customers having very high values. Employing semi-log transformation helps normalize the data, making it suitable for linear regression modeling. The semi-log transformation increased R-squared by 7 percentage points compared to a similar linear model.
- Employment status emerges as a key determinant of Customer Lifetime Value (CLV), with employed customers exhibiting higher CLV. This underscores the importance of tailoring strategies to capitalize on the potential of this segment. The number of policies held by customers positively influences CLV, suggesting that targeting customers with multiple policies can enhance CLV. The Renew Offer plays a significant role in CLV, with Renew_O1 contributing positively while offers beyond Renew_O1 have negative coefficients.
    
b. Logistic Regression: 
- Our approach employed logistic regression on the training dataset to model response rates, a method chosen for its efficacy in handling binary outcome variables. The model stuffers from false negatives where the model predicts a non-renewal but the customer actually renewed (234 cases).
- The model identified key factors affecting response rates, including demographic variables like employment status and education, and sales-related factors such as offer type and sales channel. Retired and highly educated customers, especially those with advanced degrees, showed higher response rates. Offers 3 and 4, as well as certain sales channels like call centers, led to lower response rates. Investing in offers 1 and 2, along with agent marketing, is recommended based on these findings.
    

## 🎯 Conclusions
1. The significant variables for this model were either demographic (employment status and education) or sales related (offer type and sales channel). In general, retired and highly educated (doctors or master’s degree) customers responded more often. For sales related factors, offers 3 and 4 as well as the branch, call center, and web channels each lead to lower response rates than their alternatives. 
2. Enhance focus on Employment Status: Create tailored communication for employed individuals emphasizing the security a policy provides against potential income loss.
3. Target Elderly Retired & Highly Educated Individuals Via Their Personal Agents: Capitalizes on the personal touch that can be very effective with older demographics. Higher education levels often correlate with a greater understanding of the benefits and complexities of insurance policies.

## Links
<a href="https://github.com/manling0713" class="btn btn-primary" target="_blank">
  Github Repo
</a>
