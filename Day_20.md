# Day 20 – Plotly: Pie, Histogram, Box, Scatter & Heatmap

**Date:** ____/____/______  |  **Week:** 3

## 🎯 Objective
Choose the right chart for each kind of question.

## 📚 Topics Learned
- `px.pie()` / donut charts (gender and status split)
- `px.histogram()` (age distribution)
- `px.box()` (length of stay by department)
- `px.scatter()` (age vs treatment cost)
- `px.imshow()` / heatmaps (department × month)
- Customising layout: template, fonts, margins, legends

## 🛠️ Practical Work
- Built a chart for every dimension in my dataset
- Applied one consistent colour palette across all charts
- Wrapped repeated chart code into small functions (early version of `chart_helper.py`)

```python
fig = px.histogram(df, x="Age", nbins=20, title="Patient Age Distribution")
fig.update_layout(template="plotly_white")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Pie charts with too many slices were unreadable.
- **Solution:** Limited to the top categories or used bar charts instead.

## ✅ Outcome
Learned the chart-selection rule: comparison → bar, trend → line, distribution → histogram/box, share → donut.

## 🔜 Plan for Tomorrow
Week 4 begins: introduction to Streamlit.
