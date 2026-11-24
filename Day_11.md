# Day 11 – Reading Data & First Exploration

**Date:** ____/____/______  |  **Week:** 2

## 🎯 Objective
Load external data and understand its structure.

## 📚 Topics Learned
- `pd.read_csv()` with parameters (`parse_dates`, `usecols`, `dtype`)
- `df.info()`, `df.describe()`, `df.dtypes`
- `value_counts()`, `nunique()`, `unique()`
- Saving data with `to_csv(index=False)`

## 🛠️ Practical Work
- Loaded the first version of the hospital dataset
- Checked data types, null counts, and basic statistics
- Counted patients per department and per disease

```python
df = pd.read_csv("data/raw/hospital_data.csv", parse_dates=["Admission_Date"])
df.info()
print(df["Department"].value_counts())
```

## ⚠️ Challenges & Solutions
- **Challenge:** Dates were loaded as plain text.
- **Solution:** Used `parse_dates` / `pd.to_datetime()`.

## ✅ Outcome
Can load a CSV and quickly understand what it contains.

## 🔜 Plan for Tomorrow
Selecting and filtering data with `loc`, `iloc`, and conditions.
