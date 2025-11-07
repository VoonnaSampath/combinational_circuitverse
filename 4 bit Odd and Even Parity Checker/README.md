# 4-Bit Even and Odd Parity Checker – CircuitVerse

## 🧠 Project Overview

This project demonstrates the implementation of a **4-bit Parity Checker** using [CircuitVerse](https://circuitverse.org). The circuit verifies whether a received 4-bit data stream (including parity bit) conforms to **even** or **odd** parity rules, which are widely used for **error detection** in digital communication systems.

## ✅ Key Features

- **Functionality**: Checks for parity errors in a 4-bit data input using XOR logic
- **Inputs**:
  - `D0`, `D1`, `D2`, `D3` – 4 data bits
  - `P` – Parity bit (even or odd)
- **Outputs**:
  - `Even_Error` – High if even parity check fails
  - `Odd_Error` – High if odd parity check fails
- **Controlled using**: XOR-based parity comparison logic implemented using gates or MUX (optional)

## 📂 Files Included

- `4 Bit Even and Odd Parity Checker.cv` – Raw exported CircuitVerse file
- `4 Bit Even and Odd Parity Checker.png` – Schematic image of the parity checker
- `README.md` – Documentation for this module

## 🔗 Live Simulation

[Click here to view the project on CircuitVerse](https://circuitverse.org/simulator/edit/4-bit-odd-and-even-parity-checker)

## 🛠 Tools Used

- [CircuitVerse](https://circuitverse.org) – For schematic design and simulation

---

## ⚙️ How 4-Bit Parity Checking Works

- The circuit takes 4 bits of data along with a **parity bit**.
- It performs XOR on all 5 bits (including parity).
- **If the result is 0**, parity is **correct**.
- **If the result is 1**, there is a **parity error**.

### Logic

- Even parity check: `Even_Error = D0 ⊕ D1 ⊕ D2 ⊕ D3 ⊕ P`
- Odd parity check:  `Odd_Error = ¬(D0 ⊕ D1 ⊕ D2 ⊕ D3 ⊕ P)`

---

## 📊 Truth Table Example

| D0 | D1 | D2 | D3 | P (Parity Bit) | Even_Error | Odd_Error |
|----|----|----|----|----------------|-------------|------------|
|  0 |  0 |  0 |  0 |       0        |      0      |     1      |
|  1 |  0 |  1 |  0 |       0        |      1      |     0      |
|  1 |  1 |  0 |  1 |       1        |      0      |     1      |
|  1 |  1 |  1 |  1 |       0        |      0      |     1      |
|  1 |  0 |  0 |  1 |       1        |      1      |     0      |

> `Even_Error = 1` → Error in even parity  
> `Odd_Error = 1` → Error in odd parity

---

> 💡 This project highlights real-world error detection logic found in communication systems, memories, and processors. You can extend it to support 7-bit Hamming code or combine it with encoder/decoder logic for advanced VLSI verification systems.
