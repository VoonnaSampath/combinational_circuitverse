# Combinational Circuits in CircuitVerse

This repository contains a curated collection of essential **combinational digital circuits** implemented using [CircuitVerse](https://circuitverse.org). These designs are foundational for understanding data flow and control logic in digital systems and VLSI design. Each folder represents a well-documented circuit simulation, complete with schematics and optional video demonstrations.

---

## ✅ Included Circuits

### 🔹 2-Bit Comparator

- **Function**: Compares two 2-bit binary numbers and outputs whether A > B, A = B, or A < B.
- 📁 Folder: `2bit_comparator/`

### 🔹 3x8 Decoder

- **Function**: Decodes a 3-bit binary input into 8 distinct output lines.
- 📁 Folder: `3x8_decoder/`

### 🔹 4-Bit ALU

- **Function**: Performs arithmetic and logical operations like ADD, SUB, AND, OR on 4-bit inputs.
- 📁 Folder: `4bit_alu/`

### 🔹 4-Bit Full Adder

- **Function**: Adds two 4-bit binary numbers with carry propagation.
- 📁 Folder: `4bit_full_adder/`

### 🔹 8x3 Priority Encoder

- **Function**: Encodes the highest-priority active input among 8 into a 3-bit output.
- 📁 Folder: `8x3_priority_encoder/`

---

## 📂 Folder Contents

Each subfolder typically contains:

- `circuit.cv` – Exported CircuitVerse circuit file
- `circuit.png` – Screenshot of the circuit schematic
- `README.md` – Documentation for the specific module

---

## 🧭 How to Use These Files

You can **import, view, and simulate** the circuits using [CircuitVerse](https://circuitverse.org) in just a few steps:

### 🔸 Option 1: Upload `.cv` File (Recommended)

1. Go to [https://circuitverse.org/simulator](https://circuitverse.org/simulator).  
2. Click on **File → Import**.  
3. Select the desired `.cv` file (e.g., `circuit.cv`) from the corresponding folder.  
4. The circuit will load instantly in the simulator.  
5. Click **Simulate** ▶️ to start testing inputs and observing outputs.

### 🔸 Option 2: Create New Project and Paste Components

1. Visit [CircuitVerse Simulator](https://circuitverse.org/simulator).  
2. Choose **New Circuit**.  
3. Manually recreate the design based on the provided schematic (`circuit.png`).  
4. Use the pin labels and gate connections shown in the image for accurate wiring.  
5. Save and simulate your version for practice.

### 🔸 Option 3: Use Shared Project Link

Some folders may contain a URL in their README file:

1. Copy the link.  
2. Paste it in your browser to open the circuit directly in CircuitVerse.  
3. Fork or simulate the circuit as needed.

---

## 🛠 Tools Used

- [CircuitVerse](https://circuitverse.org) – For simulation and design

---

> 💡 These circuits build the backbone of logic design concepts used in datapaths, ALUs, and control units in processor architectures.
