# 2's Complement Subtraction using Parallel Adders – CircuitVerse

## 🧠 Project Overview
This project demonstrates the implementation of **binary subtraction using the 2's complement method** with the help of **parallel adders** in [CircuitVerse](https://circuitverse.org). It shows how subtraction can be performed by taking the 2's complement of the subtrahend and adding it to the minuend using a ripple-carry adder.

## ✅ Key Features
- **Functionality**: Performs binary subtraction A - B using the 2's complement method
- **Inputs**:
  - `A[3:0]` – 4-bit Minuend
  - `B[3:0]` – 4-bit Subtrahend
- **Outputs**:
  - `D[3:0]` – 4-bit binary difference
  - `Cout` – Carry-out (optional, may be ignored in signed 2’s complement arithmetic)
- **Controlled using**: Parallel full adders, NOT gates, and an extra bit for 2’s complement (adding 1)

## 📂 Files Included
- `2's Complement Subtraction using Parallel Adders.cv` – Raw exported CircuitVerse file
- `2's Complement Subtraction using Parallel Adders.png` – Schematic image of the subtraction circuit
- `README.md` – Documentation for this module

## 🔗 Live Simulation
[Click here to view the project on CircuitVerse](https://circuitverse.org/simulator/edit/2s-compliment-subtraction-using-parallel-adder)

## 🛠 Tools Used
- [CircuitVerse](https://circuitverse.org) – For schematic design and simulation

---

## ⚙️ How 2's Complement Subtraction Works

To compute A - B using 2’s complement:
1. Take the **1’s complement** of B (invert all bits).
2. Add `1` to it to form **2’s complement** of B.
3. Add this result to A using a 4-bit ripple-carry adder.
4. Ignore carry-out for signed interpretation.

---

## 📊 Example

| A (Minuend) | B (Subtrahend) | 2's Comp(B) | A + 2's Comp(B) | Final Result |
|-------------|----------------|-------------|------------------|---------------|
|  1001 (9)   |  1100 (12)     |  0100       |     00011        | 0011 (3)      |

> The carry-out is ignored → Result is `0011` = 3

---

> 💡 This implementation is a key demonstration of how subtraction is performed in processors and ALUs using only addition logic, minimizing hardware complexity in VLSI systems.