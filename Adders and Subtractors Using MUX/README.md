# Adders and Subtractors Using MUX – CircuitVerse

## 🧠 Project Overview

This project demonstrates the implementation of basic **arithmetic logic circuits** — Half Adder, Half Subtractor, Full Adder, and Full Subtractor — using only **multiplexers (MUX)** in [CircuitVerse](https://circuitverse.org). The logic functions (XOR, AND, OR, NOT) required for arithmetic are mapped into MUX selection and input lines to eliminate the need for dedicated logic gates.

## ✅ Key Features

- **Functionality**:
  - **Half Adder**: Computes Sum and Carry for two input bits
  - **Half Subtractor**: Computes Difference and Borrow for two input bits
  - **Full Adder**: Adds two input bits and a carry-in
  - **Full Subtractor**: Subtracts two bits and a borrow-in

- **Inputs**:
  - `A`, `B` – Binary inputs
  - `Cin` / `Bin` – Carry-in (for adder) or Borrow-in (for subtractor)

- **Outputs**:
  - `Sum`, `Carry`, `Difference`, `Borrow`

- **Implemented using**: Multiplexer-based logic for all operations

## 📂 Files Included

- `Adders and Subtractors Using MUX.cv` – Complete CircuitVerse file containing all four circuits
- `HA and HS.png` – Half Adder & Half Subtractor schematic using MUX
- `FA and FS.png` – Full Adder & Full Subtractorschematic using MUX
- `README.md` – This documentation file

## 🔗 Live Simulation

[Click here to view the project on CircuitVerse](https://circuitverse.org/simulator/edit/untitled-17465415-5624-407d-9db1-ccc0cae257ce)

## 🛠 Tools Used

- [CircuitVerse](https://circuitverse.org) – For digital circuit design and simulation

---

## ⚙️ MUX-Based Implementation Overview

### 1️⃣ Half Adder Using MUX

| A | B | Sum (A⊕B) | Carry (A·B) |
|---|---|------------|--------------|
| 0 | 0 |     0      |      0       |
| 0 | 1 |     1      |      0       |
| 1 | 0 |     1      |      0       |
| 1 | 1 |     0      |      1       |

- **Sum (A⊕B)** via MUX by programming XOR truth table
- **Carry (A·B)** via MUX by mapping AND operation

---

### 2️⃣ Half Subtractor Using MUX

| A | B | Diff (A⊕B) | Borrow (¬A·B) |
|---|---|-------------|----------------|
| 0 | 0 |     0       |       0        |
| 0 | 1 |     1       |       1        |
| 1 | 0 |     1       |       0        |
| 1 | 1 |     0       |       0        |

- MUX replicates XOR for Difference  
- Borrow logic `(¬A)·B` can be expressed using MUX truth table

---

### 3️⃣ Full Adder Using MUX

| A | B | Cin | Sum | Carry |
|---|---|-----|-----|--------|
| 0 | 0 |  0  |  0  |   0    |
| 0 | 0 |  1  |  1  |   0    |
| 0 | 1 |  0  |  1  |   0    |
| 0 | 1 |  1  |  0  |   1    |
| 1 | 0 |  0  |  1  |   0    |
| 1 | 0 |  1  |  0  |   1    |
| 1 | 1 |  0  |  0  |   1    |
| 1 | 1 |  1  |  1  |   1    |

- Sum = A ⊕ B ⊕ Cin  
- Carry = (A·B) + (B·Cin) + (Cin·A)  
  → Realized using two levels of 8:1 MUX

---

### 4️⃣ Full Subtractor Using MUX

| A | B | Bin | Diff | Borrow |
|---|---|-----|------|---------|
| 0 | 0 |  0  |  0   |   0     |
| 0 | 0 |  1  |  1   |   1     |
| 0 | 1 |  0  |  1   |   1     |
| 0 | 1 |  1  |  0   |   1     |
| 1 | 0 |  0  |  1   |   0     |
| 1 | 0 |  1  |  0   |   0     |
| 1 | 1 |  0  |  0   |   0     |
| 1 | 1 |  1  |  1   |   1     |

- Diff = A ⊕ B ⊕ Bin  
- Borrow = (¬A·B) + (¬(A⊕B)·Bin)

---

> 💡 Using MUX for all arithmetic logic is a clever way to implement flexible, gate-free logic blocks — highly applicable in datapath design, configurable logic arrays, and testable VLSI systems.
