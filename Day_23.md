# Day 23 – Project Architecture, Caching & Data Loader

**Date:** ____/____/______  |  **Week:** 4

## 🎯 Objective
Restructure the project into a clean, modular architecture.

## 📚 Topics Learned
- Why single-file apps become hard to maintain
- Project structure: `utils/`, `pages/`, `scripts/`, `data/`, `assets/`
- `@st.cache_data` to avoid reloading data on every rerun
- Central configuration in `config.py` (paths, colours, bed capacity)
- Category dtype to reduce memory usage

## 🛠️ Practical Work
- Created `config.py` with file paths and theme colours
- Wrote `utils/data_loader.py` with one cached `load_data()` used by every page
- Converted text columns to `category` dtype

```python
@st.cache_data
def load_data():
    df = pd.read_csv(PROCESSED_PATH, parse_dates=["Admission_Date", "Discharge_Date"])
    for c in ["Department", "Doctor", "Gender", "Disease", "Status"]:
        df[c] = df[c].astype("category")
    return df
```

## ⚠️ Challenges & Solutions
- **Challenge:** Circular imports between modules.
- **Solution:** Kept constants in `config.py` and had utilities import only from it.

## ✅ Outcome
A scalable folder structure and a fast, cached data layer.

## 🔜 Plan for Tomorrow
Dynamic filters in `utils/filters.py`.
