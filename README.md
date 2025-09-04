## 📊 What is A/B Testing?

A/B testing (also called **split testing**) is a statistical method used to compare **two groups** and determine whether the observed difference between them is real or due to chance.  
- **Group A (Control):** Represents the current or baseline scenario.  
- **Group B (Treatment):** Represents the new or alternative scenario.  

The process involves setting up **hypotheses**, collecting data, applying statistical tests, and interpreting the results.  
This makes A/B testing one of the most widely used techniques in **product analytics, marketing, and data science**.

---

## 🧩 Problem Statement

**Business Question:**  
Do customers who pay by **card** have a different **average fare amount** than customers who pay by **cash**?

**Objective:**  
Use **hypothesis testing (two-sample t-test)** to check if there is a statistically significant difference in the average fare between the two groups.

**Hypotheses:**  
- **H₀ (Null):** μ_card = μ_cash (no difference in means)  
- **H₁ (Alternative):** μ_card ≠ μ_cash (significant difference in means)  

**Significance Level:**  
- α = 0.05 (95% confidence)

---

## 🗂️ Dataset Overview

The dataset simulates fare transaction records with the following structure:

| Column Name   | Type        | Description |
|---------------|-------------|-------------|
| `payment_type` | Categorical (`card`, `cash`) | Mode of payment |
| `fare_amount` | Numeric (float) | Fare charged for the transaction (USD) |

**Example rows:**

| payment_type | fare_amount |
|--------------|-------------|
| card         | 15.20       |
| cash         | 12.50       |
| card         | 18.75       |
| cash         | 10.40       |

This dataset is ideal for A/B testing since it naturally divides into **two groups** (`cash` vs. `card`) with a measurable outcome (`fare_amount`).

---

## 📈 Visualizations

To better understand the data and support the hypothesis testing, the following visualizations were used:

- **Histogram / Distribution Plot** → Compare fare distributions for card vs. cash
 ## 📈 Visualizations

![](Screenshot%202025-09-04%20114638.png)
![](Screenshot%202025-09-04%20120012.png)
![](Screenshot%202025-09-04%20121530.png)


These plots help verify assumptions (normality, spread) and provide intuitive insights before applying statistical tests.

---

## ✅ Conclusion

- **Statistical Test Used:** Two-sample Welch’s t-test  
- **Result:** p-value < 0.05  
- **Decision:** Reject H₀  

At a 5% significance level, there is strong evidence that the **average fare amount differs between card and cash users**.  
This implies that payment method may be associated with spending behavior, which can guide **business and pricing strategies**.

---
