#  Media Spend Recommendation Data Analysis

##  Project Overview

This project analyzes historical marketing campaign data to recommend optimal media spend across digital channels. Using a Linear Regression model, we predict Sales based on impressions from Google, Facebook, Email, and Affiliate platforms. The aim is to guide data-driven budget allocation to maximize return on investment (ROI).

---

##  Problem Statement

Marketing teams often face challenges in distributing budgets effectively across various media platforms. This project answers:
> “How can we use historical data to predict sales and optimize media spend allocation?”

---

##  Dataset Overview

The dataset (`smsd.csv`) contains 3,051 records with the following columns:

| Column                  | Description                                 |
|------------------------|---------------------------------------------|
| Division               | Marketing division (e.g., A, B, C)          |
| Calendar_Week          | Weekly identifier                           |
| Paid_Views             | Views from paid media campaigns             |
| Organic_Views          | Views from organic sources                  |
| Google_Impressions     | Impressions from Google Ads                 |
| Email_Impressions      | Impressions from Email campaigns            |
| Facebook_Impressions   | Impressions from Facebook                   |
| Affiliate_Impressions  | Impressions from affiliate marketing        |
| Overall_Views          | Total of Paid and Organic views             |
| Sales                  | Units sold (target variable)                |

---

##  Key Insights

- No missing values or nulls.
- Sales is strongly correlated with:
  - Google Impressions (0.78)
  - Facebook Impressions (0.75)
  - Email Impressions (0.74)
- Overall_Views is mostly influenced by Paid and Organic Views.
- Linear regression is a suitable model due to linear correlations.

---

##  Process Workflow

1. **Data Cleaning**
   - Validated nulls and datatypes
2. **Exploratory Data Analysis**
   - Correlation matrix and visualizations
   - Identified top predictors for Sales
3. **Model Development**
   - Trained Linear Regression model
   - Used impressions as features
4. **Evaluation**
   - R² Score and MAE for accuracy
   - Visual comparison of predicted vs actual sales
5. **Recommendation**
   - Identified high-impact channels (Google, Facebook)
   - Suggested budget shifts for performance improvement

---

##  Results

- The model showed strong predictive ability.
- Google and Facebook impressions had the highest influence on sales.
- Recommended increasing investment in these channels while reducing spend on lower-impact platforms.

---

##  Future Enhancements

- Add regularization (Ridge/Lasso) to address multicollinearity.
- Include cost per impression to estimate cost efficiency.
- Use time series or seasonal trends to enhance predictions.

---

##  Requirements

- Python 3.8+
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn

---
