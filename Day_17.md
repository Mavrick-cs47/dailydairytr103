# Day 17 – Exploratory Data Analysis (EDA)

**Date:** ____/____/______  |  **Week:** 3

## 🎯 Objective
Systematically explore the cleaned dataset to find patterns and insights.

## 📚 Topics Learned
- Descriptive statistics: mean, median, mode, std, quartiles
- Distribution analysis and skewness
- Correlation with `df.corr()`
- Identifying top and bottom performers
- Writing insight statements from numbers

## 🛠️ Practical Work
- Wrote `scripts/eda.py` that prints dataset shape, null counts, summary stats, top departments, and top diseases
- Found the correlation between length of stay and treatment cost
- Noted key insights (e.g. which age group has the longest stay)

```python
print(df[["Age", "Length_of_Stay", "Treatment_Cost"]].corr())
print(df["Disease"].value_counts().head(5))
```

## ⚠️ Challenges & Solutions
- **Challenge:** Too many numbers, unclear takeaway.
- **Solution:** Focused on 5 business questions and answered each one.

## ✅ Outcome
Clear understanding of the hospital data, ready to be visualised.

## 🔜 Plan for Tomorrow
Generating the full synthetic dataset.
