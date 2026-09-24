# Yulu Bike-Sharing: Demand Forecasting & Hypothesis Testing

## 📌 Project Overview
Yulu is India’s leading micro-mobility service provider, offering unique, sustainable vehicles for daily commutes. Recently, the company has suffered a dip in revenues. This project aims to identify the key variables influencing the demand for shared electric cycles in the Indian market.

Through Exploratory Data Analysis (EDA) and rigorous statistical hypothesis testing, this analysis provides data-driven recommendations to help Yulu optimize fleet sizing, anticipate demand fluctuations, and increase revenue.

## 🛠 Tools & Libraries Used
* **Python** (Pandas, NumPy)
* **Statistical Testing:** SciPy (`stats.ttest_ind`, `stats.f_oneway`, `stats.kruskal`, `stats.chi2_contingency`)
* **Data Visualization:** Matplotlib, Seaborn

## 📌 Business Problem

Yulu, an Indian micro-mobility company, has seen a significant dip in revenue and wants to
understand:

1. Which variables are significant in predicting the demand for shared electric cycles?
2. How well do those variables describe the electric cycle demand?

This project answers those questions using exploratory data analysis and formal statistical
hypothesis testing, rather than relying on visual impressions alone.

## 📊 Key Insights & Statistical Findings

1. **Weather & Season Drive Demand (Kruskal-Wallis, p < α):** Fall and clear weather conditions see the highest rental volumes, while Spring and rainy/snowy/foggy conditions see the lowest. Furthermore, weather and season are statistically dependent on each other (Chi-square, p < α), meaning forecast models must evaluate them together.
2. **Working Day Has No Significant Effect (Independent t-test, p = 0.226):** Average rentals are nearly identical across working days (193.0) and holidays (188.5). Fleet management should focus on intra-day redistribution (commuter spikes) rather than weekend/weekday calendar adjustments.
3. **Continuous Weather Variables Impact Volume:** Correlation analysis reveals that warmer temperatures increase rentals (Pearson r ≈ 0.39), higher humidity decreases them (r ≈ -0.32), and windspeed has a negligible effect (r = 0.10).

## 🧪 Statistical Tests Conducted
To ensure recommendations were backed by statistical significance (Alpha = 0.05), the following tests were performed:
* **2-Sample T-Test:** Analyzed the effect of Working Days vs. Holidays on rental volume.
* **ANOVA / Kruskal-Wallis:** Evaluated the impact of distinct Seasons and Weather conditions on demand.
* **Chi-Square Test of Independence:** Confirmed the dependency between Weather and Season.

## 📂 Repository Contents
* `Yulu_Final.ipynb`: The complete Python notebook containing all code, EDA, and statistical testing.
* `Yulu_Final.pdf`: A clean, presentation-ready export of the notebook featuring charts and insights.
* `yulu_bike_sharing.txt`: The raw dataset used for this analysis.

## 🚀 How to Run
1. Clone this repository.
2. Ensure you have the required libraries installed (`pip install pandas numpy scipy matplotlib seaborn`).
3. Run the `.ipynb` file in Jupyter Notebook or Google Colab, ensuring the dataset is in the same directory.

