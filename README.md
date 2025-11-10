# OOP Programming Laboratory 2

## Lab Overview
This lab continues from **OOP Lab 1 (Commit 2)**.  
The goal is to refactor the given procedural CSV processing code into an **object-oriented program**.

You will:
- Keep the provided `DataLoader` and test code unchanged.
- Implement the missing **`Table` class** to represent and manipulate tabular data.
- Verify that the test code prints the same analysis results as in Lab 1.

---

## Project Structure
oop_lab_2/
│
├── README.md
├── Cities.csv
└── data_processing.py

---

## Design Overview

### Class : `DataLoader`
**Given by professor — do not modify.**

| Responsibility | Load CSV data from file |
| --------------- | ---------------------- |
| Key method | `load_csv(filename)` → returns list of dicts |

---

### Class : `Table`
**Implemented by you.**

| Attribute | Description |
| ---------- | ------------ |
| `name` | Logical name of the table (e.g. `"cities"`) |
| `table` | List of rows (each row = dict of column→value) |

**Key methods**
| Method | Purpose |
| ------- | -------- |
| `__init__(name, rows)` | Store name and rows |
| `filter(condition)` | Return new `Table` with rows meeting `condition(row)` |
| `aggregate(func, key)` | Apply `func(list_of_column_values)` and return result |
| `__len__()` | Return row count |
| `__repr__()` | String summary for debugging |

---

## How to Run / Test
1. Make sure the structure above exists.  
2. Run the program:
   ```bash
   python data_processing.py
