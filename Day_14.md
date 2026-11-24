# Day 14 – Outliers, Feature Engineering & Week 2 Revision

**Date:** ____/____/______  |  **Week:** 2

## 🎯 Objective
Finish the cleaning pipeline and create useful derived columns.

## 📚 Topics Learned
- Detecting outliers using IQR and box-plot logic
- Creating new features: `Length_of_Stay`, `Age_Group`, `Admission_Month`
- `pd.cut()` for binning ages
- Writing a reusable cleaning script

## 🛠️ Practical Work
- Wrote `scripts/data_cleaning.py` to read the raw CSV, clean it, and save `data/processed/cleaned_hospital_data.csv`
- Added computed columns for length of stay and age groups

```python
df["Length_of_Stay"] = (df["Discharge_Date"] - df["Admission_Date"]).dt.days
df["Age_Group"] = pd.cut(df["Age"], [0, 18, 40, 60, 120],
                         labels=["Child", "Young Adult", "Adult", "Senior"])
```

## ⚠️ Challenges & Solutions
- **Challenge:** Negative stay values from wrongly ordered dates.
- **Solution:** Validated dates and removed/fixed invalid rows.

## ✅ Outcome
First reproducible cleaning pipeline: raw → processed. Week 2 complete.

## 🔜 Plan for Tomorrow
Aggregation with `groupby`.
