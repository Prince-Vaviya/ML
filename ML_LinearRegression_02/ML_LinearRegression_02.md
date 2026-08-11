# MACHINE LEARNING FUNDAMENTALS

## Assignment 3: Used Car Price Prediction — CarDekho Data

**Dataset:** Vehicle Dataset from CarDekho (*'Vehicle Dataset from CarDekho'* on Kaggle)

---

### Personalize your subset (mandatory — do this first)
Keep only cars of the fuel type assigned by `(your roll number mod 3)`:
- `0` = Petrol
- `1` = Diesel
- `2` = CNG/LPG/Electric

*If your assigned class has fewer than 150 rows, add Petrol cars until you reach at least 150 rows.*

---

### Tasks

1. **Perform EDA:** inspect data types, missing values, duplicate listings, and outliers in `selling_price` and `km_driven`.
2. **Clean the data:** engineer a `car_age` column from the year, and encode categorical columns (`fuel`, `seller_type`, `transmission`, `owner`).
3. **Create at least 5 plots using Matplotlib/Seaborn:**
   - Price distribution
   - Boxplot of `price` by `transmission` type
   - Scatterplot of `car_age` vs `price`
   - Scatterplot of `km_driven` vs `price`
   - Correlation heatmap  
   *Label everything and add a short written insight under each.*
4. **Build a Linear Regression model** predicting `selling_price` from `car_age`, `km_driven`, `fuel`, `transmission`, and `owner`.
5. **Split data 80/20** and report $R^2$ and $RMSE$ on the test set. Improve the model — handle skew in `price` with a log-transform, remove extreme outliers, add/remove features — until test $R^2$ reaches the pass condition below.
6. **Write a half-page summary** of which factors reduced resale value the most in your subset.

---

### Pass Condition
Test-set $R^2$ must be at least **0.75**. State both train and test $R^2$ in your report to show the model isn't just memorizing the training data.

---

### Deliverables
- Jupyter/Colab notebook (`.ipynb`)
- 1-page PDF summary report
