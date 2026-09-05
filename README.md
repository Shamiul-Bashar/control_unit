# Control Unit — Computer Architecture Lab 03

A **24-bit sequential datapath and control-unit design** implemented in **Logisim**, demonstrating controlled register-to-register data transfer using ROM-based control signals, a counter, multiplexer, and clocked registers.

## 📌 Project Overview

This project was developed for **Computer Architecture Lab 03**.

The circuit demonstrates a simplified processor datapath in which 24-bit data is transferred between four registers according to a predefined control sequence. The control logic uses a ROM and a 2-bit counter to generate the sequence, while a multiplexer selects the appropriate data path.

The implemented transfer sequence is:

**A → B → D → C**

This project provides a practical example of how **sequential control logic and a datapath work together** in a basic CPU architecture.

---

## 🏗️ Architecture

The design consists of four major functional sections:

### 1. 24-bit Datapath

Four 24-bit registers are used:

- **A**
- **B**
- **C**
- **D**

The registers store and transfer data according to the generated control signals.

### 2. Control Sequence Generator

A **2-bit counter** provides the sequence state/address used by the ROM.

The ROM stores the control information required for each step of the sequence.

### 3. Data Selection

A **24-bit multiplexer** selects the appropriate source data before it is transferred to the destination register.

### 4. Timing and Control

The circuit operates using:

- Clock (CLK)
- Reset (RESET)
- ROM control signals
- Splitters for control-signal distribution

---

## 🔄 Register Transfer Sequence

The primary sequence implemented by the circuit is:

~~~
A  →  B  →  D  →  C
~~~

Conceptually:

| Step | Source | Destination |
|---:|---|---|
| 1 | A | B |
| 2 | B | D |
| 3 | D | C |

The sequence is controlled synchronously using the clock signal.

---

## 🧩 Main Components

| Component | Specification | Purpose |
|---|---|---|
| Register A | 24-bit | Data storage |
| Register B | 24-bit | Data storage |
| Register C | 24-bit | Data storage |
| Register D | 24-bit | Data storage |
| Multiplexer | 24-bit | Source-data selection |
| ROM | 2-bit address / 7-bit data | Control information |
| Counter | 2-bit | Sequence generation |
| Splitters | Control-signal routing | Signal distribution |
| Clock | Digital | Sequential timing |
| Reset | Digital | Circuit initialization |

---

## ⚙️ Operation

The circuit follows a clock-driven sequence:

1. A 24-bit input is supplied to the datapath.
2. The counter generates the current sequence state.
3. The ROM uses the state to produce control information.
4. Control signals are distributed through the circuit.
5. The multiplexer selects the required 24-bit source.
6. On the appropriate clock event, the selected value is stored in the destination register.
7. The counter advances to the next sequence state.
8. The process continues through the **A → B → D → C** transfer sequence.
9. The reset input can be used to initialize the circuit.

---

## 🛠️ Technologies & Tools

- **Logisim** — Digital circuit design and simulation
- **Digital Logic** — Sequential and combinational circuit design
- **ROM** — Control-signal generation
- **Registers** — 24-bit state/data storage
- **Multiplexer** — Datapath selection
- **Counter** — Sequence/state generation
- **Splitter** — Control-signal distribution

---

## 📁 Repository Structure

~~~
control_unit/
│
├── FINAL_CA_LAB03_TASK.circ
└── README.md
~~~

### Circuit File

**FINAL_CA_LAB03_TASK.circ**

The complete Logisim circuit implementing the sequential register-transfer architecture.

---

## 🚀 How to Run

### 1. Install Logisim

Install a compatible version of **Logisim**.

### 2. Clone the Repository

~~~bash
git clone https://github.com/Shamiul-Bashar/control_unit.git
cd control_unit
~~~

### 3. Open the Circuit

Open:

~~~text
FINAL_CA_LAB03_TASK.circ
~~~

in Logisim.

### 4. Simulate

Use the Logisim simulation controls to:

- Provide 24-bit input data
- Apply/reset the circuit
- Generate clock pulses
- Observe register contents
- Observe the sequential **A → B → D → C** transfer operation

---

## 🎯 Learning Objectives

This project demonstrates practical concepts in:

- Computer architecture
- Datapath design
- Control-unit design
- Register-transfer operations
- Sequential circuit design
- ROM-based control
- Multiplexer-based data selection
- Counter-based sequencing
- Clocked register operations
- Reset and initialization
- Digital signal routing

---

## 📚 Academic Information

| | |
|---|---|
| **Course** | Computer Architecture |
| **Lab** | Lab 03 |
| **Project Type** | Sequential Datapath & Control Unit |
| **Simulation Tool** | Logisim |
| **Data Width** | 24-bit |
| **Transfer Sequence** | A → B → D → C |

---

## 👨‍💻 Author

**MD. Shamiul Basher Siam**

Computer Science & Engineering  
Khulna University of Engineering & Technology (KUET)

---

## 📄 License

This project is intended primarily for **educational and academic purposes**.

The repository may be used for learning, reference, and academic study.

---

⭐ If this project helped you understand sequential datapaths and control-unit design, consider giving the repository a star.
