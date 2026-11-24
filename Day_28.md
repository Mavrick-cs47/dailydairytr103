# Day 28 – Patient Search & CSV Export

**Date:** ____/____/______  |  **Week:** 5

## 🎯 Objective
Allow users to look up individual patients and download data.

## 📚 Topics Learned
- Searching by ID (exact match) and name (case-insensitive partial match)
- Displaying a profile card with all patient details
- `st.download_button` with `df.to_csv(index=False).encode("utf-8")`
- Handling "not found" and multiple matches

## 🛠️ Practical Work
- Wrote `utils/patient_search.py` with a search function and a profile card
- Built `pages/Patient_Search.py`
- Wrote `utils/exports.py` with a reusable `download_csv()` helper and added it to every page

```python
def download_csv(df, label, filename):
    st.download_button(label, df.to_csv(index=False).encode("utf-8"),
                       file_name=filename, mime="text/csv")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Name search was case sensitive.
- **Solution:** Used `str.contains(query, case=False, na=False)`.

## ✅ Outcome
Users can find any patient instantly and export filtered data.

## 🔜 Plan for Tomorrow
Reports suite and performance optimisation.
