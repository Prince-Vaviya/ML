# MACHINE LEARNING FUNDAMENTALS

**Assignment: Exploratory Data Analysis and Missing Value Treatment**  
**Dataset:** `student_dataset_uncleaned.csv`

This dataset contains student records with missing values, a few incorrect/outlier values, and a few duplicate rows, exactly as raw data usually looks before it is cleaned. The task is to explore the dataset, identify its problems, and handle the missing values using the most appropriate method for each column.

---

## Dataset Description

| Column | Description |
| :--- | :--- |
| `Student_ID` | Unique identifier for each student |
| `Age` | Age of the student in years |
| `Gender` | Male / Female |
| `City` | City the student resides in |
| `Study_Hours_per_day` | Average hours spent studying per day |
| `Attendance_Percentage` | Class attendance percentage |
| `Internet_Access` | Whether the student has internet access at home |
| `Part_Time_Job` | Whether the student has a part-time job (Yes/No) |
| `Exam_Score` | Final exam score out of 100 |

---

## Tasks

1. **Load the dataset and perform initial exploration:** check its `.shape`, data types, the number of missing values in each column, and the number of duplicate rows.
2. **Remove the duplicate rows** from the dataset.
3. **Use boxplots or the `describe()` function to identify outliers or impossible values** (for example, a negative number of study hours, an exam score above 100, or an unrealistic attendance percentage). Decide how you will treat each one and justify your decision in your report.
4. **For each numeric column with missing values** (`Age`, `Study_Hours_per_day`, `Attendance_Percentage`, `Exam_Score`), decide whether to use the mean or the median to fill the missing values. Base your decision on whether the column is symmetric or skewed/has outliers, and explain your reasoning for each column.
5. **For each categorical column with missing values** (`Gender`, `City`, `Internet_Access`), fill the missing values using the mode (the most frequent value in that column).
6. **After treatment, confirm that there are no missing values left** in the dataset using `isnull().sum()`, and save the cleaned dataset as `student_dataset_cleaned.csv`.
7. **Create at least 4 plots as part of your EDA:**
   - A boxplot to show outliers in `Exam_Score` or `Study_Hours_per_day`,
   - A histogram of `Age` or `Attendance_Percentage`,
   - A bar chart of the `Gender` or `City` distribution, and
   - A correlation heatmap of the numeric columns.  
   *Add a short written observation under each plot.*
8. **Write a short report (half to one page) explaining:** which method you used for each column and why, what outliers you found and how you treated them, and one interesting pattern you noticed in the data during EDA.

---

## Guidance on Choosing Mean vs Median

As a general rule: use the **mean** when a numeric column is roughly symmetric and does not have extreme outliers. Use the **median** when a column is skewed or has outliers, since the median is not affected by extreme values the way the mean is. You are expected to check each column yourself (using a histogram, boxplot, or by comparing the mean and median values) rather than assuming — this is part of what is being assessed.

---

## Deliverables

A **Jupyter or Colab notebook (`.ipynb`)** containing your code, plots, and observations; the **cleaned CSV file (`student_dataset_cleaned.csv`)**; and a **short written report** as described in Task 8.
