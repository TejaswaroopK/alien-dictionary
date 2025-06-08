# 👽 Alien Dictionary Solver

A web-based interactive tool that determines the order of characters in an alien language from a sorted list of words. This project uses **topological sorting** to derive the correct lexicographical order based on word comparisons.

---

## 📌 Project Overview

In an alien language, we don't know the order of letters. Given a sorted list of words from this language, the task is to determine the possible order of characters that justifies this sorting.

This tool implements the algorithm visually and interactively using **HTML**, **CSS**, and **Vanilla JavaScript**.

---

## ✨ Features

- 📥 Input box for entering words (space-separated).
- 🧠 Real-time evaluation of the order of characters.
- 🚨 Detects and handles invalid inputs (e.g. prefix conflicts).
- 🎨 Clean and modern user interface with responsive layout.

---

## 🛠 Technologies Used

- **HTML5** – Markup structure
- **CSS3** – Basic styling and layout
- **JavaScript (ES6)** – Core logic for solving and validating the alien character order

---

## 💡 How It Works

1. **Input Parsing**: Words are read from the text field and split.
2. **Graph Construction**: A directed graph is built where:
   - Each node is a unique character.
   - An edge from `a → b` means `a` comes before `b`.
3. **Topological Sorting**: Kahn's algorithm (BFS-based) is used to determine the character order.
4. **Validation**:
   - Ensures that longer words are not prefixes of shorter ones (`["abc", "ab"]` → invalid).
   - Detects cycles or unresolved dependencies (`Invalid Input` result).

---
