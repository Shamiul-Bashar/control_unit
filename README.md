# Control Unit — Computer Architecture Lab 03

A **24-bit sequential datapath and control-unit design** implemented in **Logisim**, demonstrating controlled register-to-register data transfer using ROM-based control signals, a counter, multiplexer, and clocked registers.

## 📌 Project Overview

This project was developed for **Computer Architecture Lab 03**.

The circuit demonstrates a simplified processor datapath in which 24-bit data is transferred between four registers according to a predefined control sequence. A ROM and 2-bit counter generate the control sequence, while a 24-bit multiplexer selects the required data path.

The implemented register-transfer sequence is:

**A → B → D → C**

This project provides a practical example of how **sequential control logic and a datapath work together** in a basic CPU architecture.

---

## 🏗️ Architecture

### 24-bit Datapath

The circuit contains four 24-bit registers:

- **A**
- **B**
- **C**
- **D**

These registers provide storage for the processor datapath and participate in the programmed transfer sequence.

### Control Sequence Generator

A **2-bit counter** generates the sequence state used to address a ROM. The ROM provides the control information required for each stage of the operation.

### Data Selection

A **24-bit multiplexer** selects the appropriate source data before it is transferred to a destination register.

### Timing & Reset

The circuit uses a clock-driven sequential design with dedicated **CLK** and **RESET** signals.

---

## 🔄 Register Transfer Sequence

~~~text
A  →  B  →  D  →  C
~~~

| Step | Source | Destination |
|---:|---|---|
| 1 | A | B |
| 2 | B | D |
| 3 | D | C |

The transfers are controlled synchronously by the clock and the generated control signals.

---

## 🧩 Main Components

| Component | Specification | Purpose |
|---|---|---|
| Register A | 24-bit | Data storage |
| Register B | 24-bit | Data storage |
| Register C | 24-bit | Data storage |
| Register D | 24-bit | Data storage |
| Multiplexer | 24-bit | Datapath/source selection |
| ROM | 2-bit address / 7-bit data | Control information |
| Counter | 2-bit | Sequence generation |
| Splitters | Control-signal routing | Signal distribution |
| Clock | Digital | Sequential timing |
| Reset | Digital | Circuit initialization |

---

## ⚙️ Operation

1. A 24-bit input is supplied to the datapath.
2. The counter generates the current sequence state.
3. The ROM uses that state to produce control information.
4. Control signals are distributed through the circuit.
5. The multiplexer selects the required 24-bit source.
6. The selected value is stored in the destination register on the appropriate clock event.
7. The counter advances to the next state.
8. The process continues through the **A → B → D → C** sequence.
9. RESET can be used to initialize the circuit.

---

## 🛠️ Technologies & Tools

- **Logisim** — Digital circuit design and simulation
- **Digital Logic** — Sequential and combinational circuit design
- **ROM** — Control-signal generation
- **24-bit Registers** — State/data storage
- **Multiplexer** — Datapath selection
- **Counter** — Sequence/state generation
- **Splitter** — Control-signal distribution

---

## 📁 Repository Structure

~~~text
control_unit/
│
├── FINAL_CA_SEQUENCE_TASK.circ
└── README.md
~~~

### Circuit File

**FINAL_CA_SEQUENCE_TASK.circ**

The complete Logisim circuit for the Computer Architecture Lab 03 sequence task.

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
FINAL_CA_SEQUENCE_TASK.circ
~~~

in Logisim.

### 4. Simulate

Use Logisim's simulation controls to:

- Provide 24-bit input data
- Apply RESET when required
- Generate clock pulses
- Observe the register values
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

This project is intended primarily for **educational and academic purposes** and may be used for learning, reference, and academic study.

---

⭐ If this project helped you understand sequential datapaths and control-unit design, consider giving the repository a star.
