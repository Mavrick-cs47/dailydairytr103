# Day 10 – Introduction to Pandas: Series & DataFrame

**Date:** ____/____/______  |  **Week:** 2

## 🎯 Objective
Get started with Pandas, the main data analysis library.

## 📚 Topics Learned
- Pandas `Series` and `DataFrame`
- Creating DataFrames from dictionaries, lists, and NumPy arrays
- Viewing data: `head()`, `tail()`, `shape`, `columns`, `index`
- Adding, renaming, and dropping columns
- Basic column arithmetic

## 🛠️ Practical Work
- Built a small patient DataFrame by hand
- Added a derived column `Cost_Per_Day`
- Renamed columns to consistent naming style

```python
import pandas as pd
df = pd.DataFrame({
    "Patient_ID": [101, 102, 103],
    "Age": [34, 58, 71],
    "Cost": [12000, 45000, 30000],
})
df["Cost_Lakh"] = df["Cost"] / 100000
```

## ⚠️ Challenges & Solutions
- **Challenge:** Mixing up column access with `df.Age` vs `df["Age"]`.
- **Solution:** Standardised on `df["Age"]`, which works for all column names.

## ✅ Outcome
Comfortable creating and inspecting DataFrames.

## 🔜 Plan for Tomorrow
Reading CSV files and exploring a dataset.
