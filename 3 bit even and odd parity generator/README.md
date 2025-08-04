# 3-Bit Even and Odd Parity Generator using MUX – CircuitVerse

## 🧠 Project Overview
This project demonstrates the implementation of a **3-bit Even and Odd Parity Generator** using **multiplexers (MUX)** in [CircuitVerse](https://circuitverse.org). The design generates parity bits for error detection by leveraging the logical properties of multiplexers to compute XOR operations across inputs.

## ✅ Key Features
- **Functionality**: Calculates both **even** and **odd** parity bits for a 3-bit input using MUX logic
- **Inputs**:
  - `A`, `B`, `C` – 3-bit input data
- **Outputs**:
  - `Even` – Even parity bit
  - `Odd` – Odd parity bit
- **Controlled using**: Logic built using 8:1 multiplexer(s) or multiple 2:1 MUX configurations to perform XOR logic

## 📂 Files Included
- `3-Bit Even and Odd Parity Generator using MUX.cv` – Raw exported CircuitVerse file
- `3-Bit Even and Odd Parity Generator using MUX.png` – Schematic image of the parity generator
- `README.md` – Documentation for this module

## 🔗 Live Simulation
[Click here to view the project on CircuitVerse](https://circuitverse.org/simulator/edit/3-bit-even-parity-and-odd-parity-generator-using-mux)

## 🛠 Tools Used
- [CircuitVerse](https://circuitverse.org) – For schematic design and logic simulation

---

## ⚙️ How Parity Generation Works

- **Even Parity**: Parity bit is `1` if the number of 1’s in the input is **odd**, making the total number of 1’s even.
- **Odd Parity**: Parity bit is `1` if the number of 1’s in the input is **even**, making the total number of 1’s odd.

> Parity = A ⊕ B ⊕ C  
> - Even Parity = A ⊕ B ⊕ C  
> - Odd Parity = ¬(A ⊕ B ⊕ C)

This XOR function is implemented using multiplexer logic by encoding truth tables into select lines and inputs.

---

## 📊 Truth Table

| A | B | C | Even Parity | Odd Parity |
|---|---|---|-------------|------------|
| 0 | 0 | 0 |     0       |     1      |
| 0 | 0 | 1 |     1       |     0      |
| 0 | 1 | 0 |     1       |     0      |
| 0 | 1 | 1 |     0       |     1      |
| 1 | 0 | 0 |     1       |     0      |
| 1 | 0 | 1 |     0       |     1      |
| 1 | 1 | 0 |     0       |     1      |
| 1 | 1 | 1 |     1       |     0      |

---

> 💡 This project highlights how multiplexers can be creatively used for logic reduction and control in error detection circuits — a core idea in digital communication and VLSI testability.