---
layout: post
title: "Autism spectrum disorder (ASD) Screening for Adults"
subtitle: "Identifying behavioral and demographic markers for rarly ASD screening using Statistical and ML models"
tags: [Python]
categories: [projects]
image: "/assets/img/asd.avif"
full-width: true
---

## 💡 Business Problem
The primary objective of the research was to explore and develop strategies for early diagnosis of ASD, emphasizing its importance in reducing healthcare costs. By identifying potential markers or indicators, the research sought to contribute to the enhancement of assessment models, ultimately leading to more effective and timely interventions for individuals with ASD.

## 📊 Dataset
The data included 21 columns, comprising 10 questionnaire questions and other variables encompassing medical and demographic background.
Data Source: https://www.kaggle.com/datasets/andrewmvd/autism-screening-on-adults/data

## 🛠️ Tools
- Tools: Python

- Skills: Chi-square test, CART model, Logistic Regression

## 🔬 Methodology
#### 1. Data Cleaning & Preprocessing
a. Encoded boolean features (Gender, Jaundice, Relative Autism, Autistic) as binary (1/0).
b. Grouped countries of residence with a count less than 50 under the Others category. Grouped Healthcare Professionals in relation variable into the Others category.
c. Remove outliers and redundant variables which correlated with other variables.
d. Mean-centering Age to decrease VIF(Variance Inflation Factor).

#### 2. Exploratory Data Analysis (EDA)
a. We observed that in this dataset, majority of examinees are between 21 and 30 years old.
![fig1](/assets/img/asd1.png)

b. Latino had the highest percentage rate of positive result.
![fig2](/assets/img/asd2.png)

### 3. Data Modeling and Analysis
a. Chi-square Test  
Initially, we employed the Chi-square test as a preliminary step to identify which variables were statistically significant and should be included in our predictive models.
    
b. Classification And Regression Trees Model (CART)  
We noticed that the CART model mainly splits based on the 10 questions about behavior related to autism. This means these questions are important for figuring out if someone might have autism. 

c. Logistic Regression Model  
The variables linked to behavioral questions have larger coefficients compared to other variables in our model. This means that behaviors related to autism play a crucial role in predicting autism traits compared to other factors we looked at. 
![fig3](/assets/img/asd3.png)
    

## 🎯 Conclusions
1. Q9 (The inability to understand what someone is thinking, just by looking at their face) is a variable which is most significantly related to traits of ASD.
2. We cannot recommend someone for a full ASD assessment on the basis of their Age
3. Jaundice, Relatives with Autism, and ethnicity are more significant factors to screen ASD.

## Links
<a href="https://github.com/manling0713/Autism-Screening/tree/main" class="btn btn-primary" target="_blank">
  Github Repo
</a>
