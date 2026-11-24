# Day 6 – File Handling, Exceptions & Virtual Environments

**Date:** ____/____/______  |  **Week:** 1

## 🎯 Objective
Read and write files safely and manage project dependencies.

## 📚 Topics Learned
- Opening files with `open()` and the `with` statement
- Reading/writing text files and CSV files (`csv` module)
- Exception handling: `try`, `except`, `finally`, `raise`
- Creating a virtual environment with `python -m venv venv`
- Managing packages with `pip install` and `requirements.txt`

## 🛠️ Practical Work
- Wrote patient records to a CSV file and read them back
- Added error handling for missing files
- Created my first virtual environment and generated `requirements.txt` with `pip freeze`

```python
try:
    with open("patients.csv") as f:
        print(f.readline())
except FileNotFoundError:
    print("File not found.")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Virtual environment would not activate on Windows.
- **Solution:** Used `venv\Scripts\activate` instead of the Linux/macOS command.

## ✅ Outcome
Able to work with files safely and keep project dependencies isolated.

## 🔜 Plan for Tomorrow
Object-oriented programming basics and Week 1 revision.
