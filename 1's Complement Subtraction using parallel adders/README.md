# 1's Complement Subtraction using Parallel Adders – CircuitVerse

## 🧠 Project Overview

This project demonstrates the implementation of **binary subtraction using 1's complement** technique with the help of **parallel adders** in [CircuitVerse](https://circuitverse.org). The design illustrates how subtraction can be achieved by inverting the bits of the subtrahend and adding it to the minuend using a ripple-carry structure, followed by end-around carry handling.

## ✅ Key Features

- **Functionality**: Performs binary subtraction A - B using the 1's complement method
- **Inputs**:
  - `A[3:0]` – 4-bit Minuend
  - `B[3:0]` – 4-bit Subtrahend
- **Outputs**:
  - `D[3:0]` – 4-bit binary difference
  - `Cout` – End-around carry flag (if used)
- **Controlled using**: Parallel full adders, NOT gates for 1’s complement, and logic for carry adjustment

## 📂 Files Included

- `1's Complement Subtraction using Parallel Adders.cv` – Raw exported CircuitVerse file
- `1's Complement Subtraction using Parallel Adders.png` – Schematic image of the subtraction circuit
- `README.md` – Documentation for this module

## 🔗 Live Simulation

[Click here to view the project on CircuitVerse](https://circuitverse.org/simulator/edit/1-s-compliment-subtraction-using-parallel-adders)

## 🛠 Tools Used

- [CircuitVerse](https://circuitverse.org) – For schematic design and simulation

---

## ⚙️ How 1's Complement Subtraction Works

To compute A - B using 1’s complement:

1. Take 1’s complement of `B` (invert each bit).
2. Add it to `A` using a 4-bit ripple-carry adder.
3. If there is a carry-out, add `1` to the result (end-around carry).
4. If no carry, the result is in 1's complement form → take complement again for negative result.

---

## 📊 Example

| A (Minuend) | B (Subtrahend) | 1's Comp(B) | A + 1's Comp(B) | Final Result |
|-------------|----------------|-------------|------------------|---------------|
|  1010 (10)   |  1001 (9)      |  0110     |     0111        | 0001 (1)      |

> Carry-out exists → add it back → final result is 1

---

> 💡 This project demonstrates how arithmetic logic can be built from simple building blocks (like full adders) to perform complex operations like subtraction—an essential part of ALU and datapath design in VLSI.
