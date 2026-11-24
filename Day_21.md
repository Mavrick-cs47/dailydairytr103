# Day 21 – Introduction to Streamlit

**Date:** ____/____/______  |  **Week:** 4

## 🎯 Objective
Turn Python scripts into an interactive web app.

## 📚 Topics Learned
- What Streamlit is and how the script reruns on every interaction
- Installing and running: `streamlit run app.py`
- Text elements: `st.title`, `st.header`, `st.markdown`, `st.write`
- Displaying DataFrames: `st.dataframe`, `st.table`
- Showing Plotly charts: `st.plotly_chart`

## 🛠️ Practical Work
- Created my first `app.py` that loads the cleaned CSV and shows a table and one chart
- Opened the app at `localhost:8501`

```python
import streamlit as st
import pandas as pd

st.title("Hospital Analytics Dashboard")
df = pd.read_csv("data/processed/cleaned_hospital_data.csv")
st.dataframe(df.head(50))
```

## ⚠️ Challenges & Solutions
- **Challenge:** Running `python app.py` showed nothing.
- **Solution:** Streamlit apps must be launched with `streamlit run`.

## ✅ Outcome
First web-based version of my analysis running in the browser.

## 🔜 Plan for Tomorrow
Widgets, sidebar, columns, and layout.
