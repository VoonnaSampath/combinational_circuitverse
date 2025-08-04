BCD to 7 Segment Display
# BCD to 7-Segment Display Decoder using Logic Gates – CircuitVerse

## 🧠 Project Overview
This project demonstrates the implementation of a **BCD (Binary-Coded Decimal) to 7-Segment Display Decoder** using only **basic logic gates** in [CircuitVerse](https://circuitverse.org). It accepts a 4-bit BCD input (0000 to 1001) and lights up the appropriate segments (`a` to `g`) on a common cathode 7-segment display.

The design avoids ROM or multiplexers, instead relying on **minimized Boolean expressions** derived from truth tables and Karnaugh Maps for each segment.

## ✅ Key Features

- **Functionality**: Converts 4-bit BCD input (0–9) into control signals for a 7-segment display
- **Inputs**:
  - `A`, `B`, `C`, `D` – BCD input (4 bits)
- **Outputs**:
  - `a`, `b`, `c`, `d`, `e`, `f`, `g` – Control lines for each segment
- **Design Style**: Purely logic-gate based (AND, OR, NOT, NAND)

## 📂 Files Included

- `BCD to 7 Segment Display.cv` – Raw CircuitVerse file
- `BCD to 7 Segment Display.png` – Schematic image of the entire circuit
- `README.md` – Documentation for this module

## 🔗 Live Simulation

[Click here to view the project on CircuitVerse](https://circuitverse.org/simulator/edit/bcd-to-7-segment-display-421e74cc-18e9-404c-87b6-40cdabe55c69)

## 🛠 Tools Used

- [CircuitVerse](https://circuitverse.org) – For schematic design and logic simulation

---

## ⚙️ Segment Control Logic

Each of the 7 output segments (`a` to `g`) is driven by a unique Boolean function derived from the BCD input values for digits `0` to `9`. The logic for each segment is implemented **directly using gates**, with minimized expressions.

### Segment Logic Examples:

- **Segment a**  
  `a = C+BD+B'D'+A`

- **Segment b**  
  `b = B' C'D' CD`

- **Segment c**  
  `c = D B C' `

- **Segment d**  
  `d = B'D' B'C BC'D CD' A`

- **Segment e**  
  `e = B'D' CD'`

- **Segment f**  
  `f = C'D' BC' BD' A`

- **Segment g**  
  `g = B'C BC' A CD'`

> Note: Logic may vary depending on whether **common cathode** or **common anode** display is used. Above logic is tailored for **common cathode** displays where high = ON.

---

## 📊 Truth Table: BCD Input → 7-Segment Output

| Decimal | BCD (D3 D2 D1 D0) | a | b | c | d | e | f | g |
|---------|-------------------|---|---|---|---|---|---|---|
|   0     |       0000        | 1 | 1 | 1 | 1 | 1 | 1 | 0 |
|   1     |       0001        | 0 | 1 | 1 | 0 | 0 | 0 | 0 |
|   2     |       0010        | 1 | 1 | 0 | 1 | 1 | 0 | 1 |
|   3     |       0011        | 1 | 1 | 1 | 1 | 0 | 0 | 1 |
|   4     |       0100        | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
|   5     |       0101        | 1 | 0 | 1 | 1 | 0 | 1 | 1 |
|   6     |       0110        | 1 | 0 | 1 | 1 | 1 | 1 | 1 |
|   7     |       0111        | 1 | 1 | 1 | 0 | 0 | 0 | 0 |
|   8     |       1000        | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
|   9     |       1001        | 1 | 1 | 1 | 1 | 0 | 1 | 1 |

> Inputs from 1010 (10) to 1111 (15) are **invalid BCD** and can optionally output all segments OFF.

---

## 🔍 Educational Highlights

- Shows real-world **decoder logic** from inputs to display control
- Strengthens concepts of **Boolean expression minimization**
- Demonstrates how **gates can fully replace lookup tables** or ROMs in small-scale circuits
- Excellent as a **portfolio-ready project** for digital design or VLSI track

---