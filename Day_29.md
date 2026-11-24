# Day 29 – Reports Suite & Performance Optimisation

**Date:** ____/____/______  |  **Week:** 5

## 🎯 Objective
Finish the five reports and make the app fast.

## 📚 Topics Learned
- Designing report tables that managers can act on
- Using tabs to organise multiple reports on one page
- Performance tuning: caching, category dtypes, single-pass filtering, avoiding repeated `groupby` calls

## 🛠️ Practical Work
- Built `pages/Reports.py` with Monthly, Department, Revenue, Disease, and Average Stay reports
- Added a CSV download button for each report
- Profiled the app and removed redundant computations

## ⚠️ Challenges & Solutions
- **Challenge:** The app slowed down with the full dataset.
- **Solution:** Cached the loader, used category dtypes, and filtered only once per run.

## ✅ Outcome
All five reports are complete, exportable, and load quickly.

## 🔜 Plan for Tomorrow
Final testing, README, and project presentation.
