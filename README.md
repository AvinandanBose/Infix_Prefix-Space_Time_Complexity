# Infix To Prefix Conversion: Space & Time Complexity Analysis

![GitHub repo size](https://img.shields.io/github/repo-size/AvinandanBose/Infix_Prefix-Space_Time_Complexity)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 📌 About The Repository
This repository explains the mechanics of converting an **Infix** expression to a **Prefix** expression. It highlights the step-by-step approach, contrasts it with Postfix conversion, and provides an in-depth analysis of the Space and Time complexities involved in the algorithm.

## 📂 Topics & Resources Included

The repository contains detailed PDF documents breaking down the core concepts:
* **Infix To Prefix Conversion:** Step-by-step logic, reversing expressions, and applying stack operations.
* **Space Complexity Analysis:** A dedicated look into how memory is allocated and utilized during the conversion process.

## ⚙️ How The Conversion Works

The stack operations (Push, Pop) remain mostly the same as in Postfix conversion, but the overarching approach changes:

1. **Given Infix Expression:** `(a + b)`
2. **Postfix vs Prefix:** * Postfix equivalent: `ab+`
   * Prefix equivalent: `+ab`
3. **The Approach:**
   * Scan the infix expression from **right to left** (last to first).
   * After pushing to the stack and forming a temporary expression, you might end up with `ba+`.
   * For example, in an array where `a[0] = b`, `a[1] = a`, and `a[2] = +`.
   * Swap and reverse these elements to yield the final Prefix expression: `+ab`.

---

## ⏱️ Time Complexity Analysis: `O(N)`

Overall, the time complexity of the program is **`O(N)`**, where `N` is the length of the infix expression. Here is the breakdown:

* Stack operations (`push` and `pop`) take **`O(1)`** time each.
* Traversing the infix string from last to first takes **`O(N)`** time.
* Popping everything from the stack and adding it to the prefix expression takes **`O(N)`** time in the worst case.
* Reversing the final string expression using a loop takes **`O(N)`** time.
* Freeing up memory takes **`O(1)`** time.
* **Total Time Complexity = `O(1) + O(N) + O(N) + O(N) = O(N)`**.

## 💾 Space Complexity Analysis: `O(N)`

Overall, the space complexity of the program is **`O(N)`**, where `N` is the length of the infix expression. Here is the breakdown:

* **Prefix Expression String:** Allocating memory (`malloc`) for the resulting prefix expression string takes **`O(N)`** space (`length * sizeof(char)`).
* **Stack Memory:** Creating a stack of size `len` to store the characters requires **`O(N)`** space. Pushing `N` times takes up this `O(N)` space.
* **Variables & In-place Operations:** Extra variables (`len, i, j, start, end, temp`) take constant space **`O(1)`**. Adding elements and swapping array characters take **`O(1)`** auxiliary space.
* **Total Space Complexity = `O(N) (stack) + O(1) (variables) = O(N)`**.

## 💻 Code Implementation

Looking for the actual code? The C++ implementation of the Infix to Prefix conversion can be found in the following repository:
👉 **[C++ - Data Structures Repository](https://github.com/AvinandanBose/CPLUSPLUS_DataStructure)**

## 📜 License
This repository is licensed under the [MIT License](LICENSE).
