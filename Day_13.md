# Day 13 – Data Cleaning: Missing Values, Duplicates & Types

**Date:** ____/____/______  |  **Week:** 2

## 🎯 Objective
Learn to turn messy raw data into analysis-ready data.

## 📚 Topics Learned
- Detecting nulls with `isnull().sum()`
- Handling missing values: `dropna()`, `fillna()`, mean/median/mode imputation
- Removing duplicates with `drop_duplicates()`
- Converting types with `astype()` and `pd.to_datetime()`
- Cleaning text: `str.strip()`, `str.title()`, `str.replace()`

## 🛠️ Practical Work
- Cleaned inconsistent department names and whitespace
- Filled missing ages with the median and missing insurance with "Unknown"
- Removed duplicate patient records

```python
df["Age"] = df["Age"].fillna(df["Age"].median())
df["Department"] = df["Department"].str.strip().str.title()
df = df.drop_duplicates(subset="Patient_ID")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Deciding between dropping and filling nulls.
- **Solution:** Dropped only when the field was critical (ID); filled otherwise.

## ✅ Outcome
Understood that clean data is the foundation of reliable analytics.

## 🔜 Plan for Tomorrow
Outliers, derived columns, and building `data_cleaning.py`.
