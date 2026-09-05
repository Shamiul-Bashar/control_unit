# Control Unit — Computer Architecture Lab 03

A digital logic and computer architecture project implemented in **Logisim**, featuring a 24-bit register-based datapath, ROM-based control logic, multiplexing, and sequential control circuitry.

---

## 📌 Project Overview

This project was developed as part of **Computer Architecture Lab 03**.

The design demonstrates how a simplified processor datapath can be controlled using digital logic components. The circuit combines registers, a ROM-based control mechanism, multiplexers, splitters, counters, and clock/reset signals to demonstrate controlled data movement and sequential operation.

The primary objective is to understand the interaction between **control logic, registers, memory, and datapath components** in a basic CPU architecture.

---

## 🧩 Main Components

- **24-bit Input Data**
- **24-bit Registers:** A, B, C, and D
- **ROM-based Control Logic**
- **2-bit Counter**
- **24-bit Multiplexer**
- **Splitters**
- **Clock Signal**
- **Reset Signal**
- **Control and Data Routing Logic**

---

## 🏗️ Architecture

The design consists of two major parts:

### Datapath

The datapath stores and transfers 24-bit data between registers.

```
             24-BIT INPUT
                  │
                  ▼
              ┌───────┐
              │  MUX  │
              └───┬───┘
                  │
        ┌─────────┼─────────┐
        ▼         ▼         ▼
     ┌─────┐   ┌─────┐   ┌─────┐   ┌─────┐
     │  A  │   │  B  │   │  C  │   │  D  │
     │ 24b │   │ 24b │   │ 24b │   │ 24b │
     └─────┘   └─────┘   └─────┘   └─────┘
        ▲         ▲         ▲         ▲
        └─────────┴─────────┴─────────┘
                 Control Logic
```

### Control Unit

The control section generates signals required to control data movement and register operations. A ROM and counter provide control information, while splitters distribute control signals through the circuit.

---

## ⚙️ How It Works

1. A 24-bit input is supplied to the datapath.
2. The control logic determines the required data-routing operation.
3. The multiplexer selects the appropriate data source.
4. Selected data is transferred toward the destination register.
5. Registers store data on the appropriate clock event.
6. ROM and counter logic provide sequential control information.
7. Reset initializes the relevant circuit state.

This demonstrates the fundamental relationship between a **control unit and datapath** in processor architecture.

---

## 🛠️ Technologies & Tools

| Technology | Purpose |
|---|---|
| **Logisim** | Digital circuit design and simulation |
| **Digital Logic** | Control and datapath implementation |
| **ROM** | Control information storage |
| **Registers** | 24-bit data storage |
| **Multiplexer** | Datapath selection |
| **Counter** | Sequential control/address generation |

---

## 📁 Repository Structure

```
control_unit/
│
├── FINAL_CA_LAB03_TASK.circ
└── README.md
```

### Circuit File

**FINAL_CA_LAB03_TASK.circ** — The main Logisim project containing the digital logic circuit.

---

## 🚀 How to Run

### 1. Install Logisim

Install a compatible version of **Logisim**.

### 2. Clone the Repository

```bash
git clone https://github.com/Shamiul-Bashar/control_unit.git
```

### 3. Open the Circuit

Open `FINAL_CA_LAB03_TASK.circ` in Logisim.

### 4. Simulate

Use Logisim's simulation controls to provide input data, clock signals, and reset signals, then observe the datapath and control circuitry.

---

## 🎯 Learning Objectives

This project provides practical experience with:

- Digital logic circuit design
- CPU datapath architecture
- Control-unit design
- Register-based data storage
- Multiplexer-based data selection
- ROM-based control logic
- Sequential circuits
- Clocked operations
- Reset mechanisms
- Signal splitting and routing
- Computer architecture fundamentals

---

## 📚 Academic Context

| | |
|---|---|
| **Course** | Computer Architecture |
| **Lab** | Lab 03 |
| **Project Type** | Digital Logic / CPU Architecture |
| **Simulation Tool** | Logisim |

---

## 👨‍💻 Author

**MD. Shamiul Basher Siam**

Computer Science & Engineering  
Khulna University of Engineering & Technology (KUET)

---

## 📄 License

This project is intended primarily for educational and academic purposes. You are welcome to study and reference the implementation for learning purposes.

---

⭐ If you find this project useful for learning digital logic or computer architecture, consider giving the repository a star.
