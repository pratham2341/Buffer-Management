# 🧠 Buffer Management System (C++)

A simulation of how real-world databases manage memory efficiently by implementing various **page replacement strategies** such as **LRU**, **MRU**, and **CLOCK**. The system is designed in **C++** and measures the number of disk I/O operations to evaluate the performance of each algorithm under realistic workloads.

---

## 📌 Overview

Databases load data pages from disk into a limited-size buffer (memory). When the buffer is full, a **buffer manager** decides **which page to evict** to make space for a new one. This project implements and compares:

- ✅ **LRU** (Least Recently Used)
- ✅ **MRU** (Most Recently Used)
- ✅ **CLOCK** (a circular, efficient approximation of LRU)

The system evaluates which strategy performs best based on **disk I/O operations**.

---

## 🚀 Key Features

- 🧠 **Custom buffer pool design** with frame metadata:
  - Pin count
  - Dirty bit
  - Reference bit
- ⚙️ **Implementation of three page replacement algorithms**
- 📊 **Real workload simulation** using CSV files (Employee & Company data)
- 📉 **Performance analysis based on I/O count**
- 📁 Clean and modular C++ code using STL

---

## 🧪 Testing Methodology

- A **join query** is simulated using two CSV files.
- The access pattern is tested in two cases:
  - **Sorted (Sequential)** – Best case scenario
  - **Shuffled (Randomized)** – Realistic access pattern
- For each strategy, the total number of **disk I/O operations** is recorded.

### 📈 Sample Results:

| Strategy | I/O Operations |
|----------|----------------|
| CLOCK    | 46.38          |
| LRU      | 50.22          |
| MRU      | 67.82          |

---

## 🧰 Tech Stack

- **Language:** C++
- **Environment:** g++ / VS Code
- **Data Source:** CSV files
- *(Optional for expansion: SQLite for real disk simulation)*

---



