# MACHINE LEARNING FUNDAMENTALS

## Assignment 4: Student Exam Score Prediction — Study Habits Dataset

**Dataset:** Student Habits vs Academic Performance (*'Student Habits vs Academic Performance'* or similar on Kaggle)

---

### Personalize your subset (mandatory — do this first)
Keep only rows where `gender` matches your own gender, AND `study_hours >= (your roll number mod 5) + 1`. If this leaves fewer than 150 rows, drop the study-hours condition and keep the gender filter only.

---

### Tasks

1. **Perform EDA:** check missing values, duplicates, and outliers in exam scores and study hours.
2. **Clean the data:** handle missing values and encode categorical fields (e.g., part-time job status, internet access).
3. **Create at least 5 plots using Matplotlib/Seaborn:**
   - Score distribution
   - Scatterplot of `study_hours` vs `score`
   - Boxplot of `score` by `part-time-job` status
   - Correlation heatmap
   - Bar chart of average `score` by a `sleep-hours` bucket  
   *Label everything and add a short written insight under each.*
4. **Build a Linear Regression model** predicting exam score from `study_hours` plus at least 3 other features.
5. **Split data 80/20** and report $R^2$ and $RMSE$ on the test set. Refine the model — feature scaling, dropping weak/noisy features, handling outliers — until test $R^2$ reaches the pass condition below.
6. **Write a half-page summary** of which habits most affected exam performance in your subset.

---

### Pass Condition
Test-set $R^2$ must be at least **0.70**.

---

### Deliverables
- Jupyter/Colab notebook (`.ipynb`)
- 1-page PDF summary report
