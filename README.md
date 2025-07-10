# better_sort
# Multithreaded Merge Sort in C++
Author: Vikram Malhotra  
Machine: MacBook Pro M1 (2020)  
Language: C++11  

## 🔍 Overview
This project implements a **multithreaded Merge Sort** algorithm using modern C++11 features like `std::thread`. The goal is to improve performance by parallelizing parts of the recursive sorting process on multi-core systems like the M1.

## 🧠 Main Idea
While analyzing the recursive structure of Merge Sort, I realized that parts of the recursion could be **executed in parallel** using threads. The key is to create new threads only when the recursion depth is below a certain threshold, preventing thread overhead.

The time and space complexity remain the same (`O(n log n)`), but multithreading provides a **performance boost on large datasets**.

## ⚙️ How to Use
- No external libraries required.
- Pure C++11 implementation.
- Works cross-platform — tested on macOS (M1), should also work on Linux and Windows.

### 🛠 Usage
1. Include `mergeSortMT.hpp` in your C++ project.
2. Use the `mergeSortMT` function as you would any sorting algorithm.
3. Compile using:
```bash
g++ -std=c++11 -pthread main.cpp -o mergesort
```

## 📈 Benchmarking
This implementation includes benchmarking comparisons with `std::sort` to demonstrate the effect of multithreading on large input sizes (e.g., 1M+ elements).

## 📂 File Structure
- `mergeSortMT.hpp` – Core logic for multithreaded Merge Sort
- `main.cpp` – Example usage and benchmarking
- `.gitignore` – Ignores build and system-specific files
- `README.md` – This file

## 📌 Notes
- This implementation was written and tested by me on a MacBook Pro M1.
- Useful for learning multithreading, templates, and performance optimization in C++.

Feel free to fork and modify!
