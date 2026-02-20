# 🧮 Advanced Calculator — Python (OOP)

> A feature-rich, menu-driven calculator built in Python using Object-Oriented Programming. Covers arithmetic, statistics, and percentage calculations — built and run in Google Colab.

---

## 📌 About This Project

This project is a **console-based Advanced Calculator** built entirely with Python and core OOP principles. It was developed as a hands-on learning project to practice class design, type casting, input validation, and statistical logic — all within a single clean Jupyter Notebook.

**Platform:** Google Colab / Jupyter Notebook  
**Language:** Python 3  
**Paradigm:** Object-Oriented Programming (OOP)

---

## ✨ Features

| #  | Feature | Description |
|----|---------|-------------|
| 1  | ➕ Addition | Add two numbers |
| 2  | ➖ Subtraction | Subtract two numbers |
| 3  | ✖️ Multiplication | Multiply two numbers |
| 4  | ➗ Division | Divide with zero-division error handling |
| 5  | 📊 Modulus | Find the remainder of division |
| 6  | 📈 Statistics | Mean, Median, Mode, Range, Sum, Count on a list of numbers |
| 7  | 📊 Percentage Calculator | 3 modes: X% of Y, X is what % of Y, % increase/decrease |
| 8  | ❌ Exit | Graceful exit with farewell message |

---

## 🧠 Concepts Used

- **OOP (Object-Oriented Programming)** — entire calculator is a `Calculator` class with clearly defined methods
- **Type Casting** — smart input parsing: auto-detects `int` vs `float` based on user input
- **Input Validation** — `try/except` blocks prevent crashes from invalid input
- **`collections.Counter`** — used to calculate Mode efficiently
- **`typing` module** — `List` and `Union` type hints for clean, readable method signatures
- **`KeyboardInterrupt` handling** — graceful exit on Ctrl+C
- **Statistics from scratch** — Mean, Median, and Mode implemented manually (no `statistics` module)

---

## 📂 Project Structure

```
📁 advanced-calculator/
├── calculator.ipynb    # Main Jupyter Notebook (full source + live output)
└── README.md           # This file
```

---

## 🚀 How to Run

### ▶️ Option 1 — Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `calculator.ipynb`
3. Click **Runtime → Run All**
4. Interact with the menu in the output cell

### 💻 Option 2 — Local (Jupyter)
```bash
# Install Jupyter if needed
pip install notebook

# Launch
jupyter notebook calculator.ipynb
```

### 🐍 Option 3 — Run as a Python Script
Copy the source from the notebook cell into a `.py` file and run:
```bash
python calculator.py
```

---

## 🖥️ Sample Output

```
🧮 Advanced Calculator
==================================================

🧮 Calculator Menu
==============================
1. ➕ Addition
2. ➖ Subtraction
3. ✖️  Multiplication
4. ➗ Division
5. 📊 Modulus (%)
6. 📈 Statistics (Mean, Median, Mode, Average)
7. 📊 Percentage Calculator
8. ❌ Exit
------------------------------
Enter your choice (1-8): 6

📝 Enter numbers separated by spaces:
Numbers: 54 65 76 43 89

📊 Statistical Analysis for: [54, 65, 76, 43, 89]
----------------------------------------
📈 Mean (Average): 65.40
📊 Median: 65
🎯 Mode: No mode (all values appear equally)
📏 Range: 46
🔢 Count: 5
📊 Sum: 327
```

---

## 🔧 Class Design Overview

```python
class Calculator:
    ├── get_number_input()       # Smart int/float type casting with validation
    ├── get_numbers_list()       # Parse space-separated numbers for stats
    ├── addition()               # a + b
    ├── subtraction()            # a - b
    ├── multiplication()         # a × b
    ├── division()               # a ÷ b  (zero-division safe)
    ├── modulus()                # a % b  (zero-division safe)
    ├── calculate_mean()         # sum / count
    ├── calculate_median()       # handles even & odd list lengths
    ├── calculate_mode()         # via Counter — handles no-mode & multi-mode
    ├── statistics_menu()        # full stats analysis on a number list
    ├── percentage_calculator()  # 3-mode percentage tool
    ├── display_menu()           # prints the menu UI
    └── run()                    # main loop (while True + graceful exit)
```

---

## 📦 Dependencies

Only Python standard library — no external packages required:

```python
import math
from collections import Counter
from typing import List, Union
```

---

## 🎯 What I Learned

- Structuring a project using **OOP** instead of plain functions
- Writing **reusable methods** with single responsibilities
- Implementing **robust input handling** using loops and exceptions
- Computing **statistics manually** to understand the underlying logic
- Designing a **menu-driven CLI app** with a smooth user experience

---

## 👤 Author

**Student Name** — B.Sc (CSE), Haldia Institute of Management  
Mentored by: **SK Sahil** (AI Developer & Tutor) — [@Code_ScholarEU](https://www.instagram.com/code_scholar_eu/)

- 🐙 GitHub: `https://github.com/your-username`
- 📧 Email: `your-email@example.com`

---

## 📄 License

This project is open for personal and educational use. Feel free to fork, adapt, and learn from it.

---

*Built with Python 🐍 in Google Colab — no frameworks, no libraries, just logic.*
