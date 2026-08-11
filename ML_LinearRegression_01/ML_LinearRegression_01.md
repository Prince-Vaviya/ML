# MACHINE LEARNING FUNDAMENTALS

## Assignment 2: House Price Prediction — Bengaluru Housing Data

**Dataset:** Bengaluru House Price dataset (*'Bengaluru House Price Data'* on Kaggle)

---

### Personalize your subset (mandatory — do this first)
Filter the dataset to locations whose name starts with the same letter as your first name, AND keep only rows with `bathrooms >= (last digit of your roll number)`. If this leaves fewer than 150 rows, drop the bathroom condition and keep the location filter only.

---

### Tasks

1. **Perform EDA:** check shape, data types, missing values, duplicates, and outliers in `price` and `area`.
2. **Clean the data:** handle missing values, convert `total_sqft` ranges (e.g. `'2100-2850'`) to a single numeric value, and create a new `price_per_sqft` column.
3. **Create at least 5 plots using Matplotlib/Seaborn:**
   - Price distribution
   - Boxplot of `price` by `BHK`
   - Scatterplot of `area` vs `price`
   - Correlation heatmap
   - Bar chart of average `price` by `location`  
   *Label every axis and title, and write a 2-3 line insight under each plot.*
4. **Build a Linear Regression model** predicting `price` from `area`, `BHK`, `bathrooms`, and `location` (one-hot encoded).
5. **Split data 80/20 (train/test)** and report $R^2$ and $RMSE$ on the test set. Iterate — remove outliers, try a log-transform of `price`, add or drop features — until test $R^2$ reaches the pass condition below.
6. **Write a half-page summary** of which factors most affected price and why your final model performs as it does.

---

### Pass Condition
Test-set $R^2$ must be at least **0.75**. Marks are reduced for models that hit this only by overfitting (e.g., huge gap between train and test $R^2$) — mention both scores in your report.

---

### Deliverables
- Jupyter/Colab notebook (`.ipynb`)
- 1-page PDF summary report
