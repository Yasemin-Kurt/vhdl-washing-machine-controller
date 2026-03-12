# VHDL Washing Machine Controller

Design and simulation testing of a washing machine control unit using VHDL and finite state machines (FSM).

## Project Overview

This project presents the design and simulation of a washing machine control unit using **VHDL** and a **Finite State Machine (FSM)** based architecture.

While modern washing machines are typically controlled by **microcontroller-based embedded systems**, this project models the control algorithm directly at the **hardware level** using VHDL. The goal is to demonstrate how a complex appliance control algorithm can be implemented through a deterministic FSM structure.

The system manages washing machine operations such as **program selection, temperature control, washing, rinsing, and spinning stages**. Timing of each operation is handled using **counter-based hardware timing mechanisms**, ensuring deterministic and predictable behavior.

The design and verification process was carried out using the **Vivado development environment**, where behavioral simulations were performed using a testbench to validate state transitions and timing behavior.

This project was developed as a **Bachelor's Graduation Project** and serves as an educational reference for **FPGA-based control system design**.

---

# Features

## Program and Temperature Modes

The controller supports multiple washing programs based on common household washing machine modes.

Supported programs include:

- Cotton  
- Synthetic  
- Mixed  
- Delicate / Silk  
- Hand Wash  
- Jeans / Dark Clothes  
- Allergy / Baby  
- Sportswear  
- Shirts  
- Quick Wash  

Each program is associated with specific temperature options such as:

- 20°C
- 30°C
- 40°C
- 60°C
- 90°C
- ❄️°C

Invalid program–temperature combinations are prevented through FSM logic.

---

## Counter-Based Timing Control

Instead of software delays, operation durations are controlled using **hardware counters driven by the FPGA clock signal**.

Each washing stage (washing, rinsing, spinning, etc.) runs for a defined number of clock cycles, ensuring:

- deterministic timing behavior  
- hardware-level time control  
- independence from processor execution flow

These durations can be scaled depending on the **system clock frequency** of the target FPGA.

---

# Simulation and Verification

The design was verified using **behavioral simulations in Vivado**.

A dedicated **testbench** was created to simulate system inputs and observe FSM state transitions through waveform analysis.

Simulation results confirm that:

- state transitions occur as expected  
- operation timing follows the defined counter-based control  
- the FSM structure correctly represents the washing process flow

⚠️ Note:  
The provided testbench does **not cover all possible system states and scenarios**, but demonstrates the fundamental functionality of the control unit.

---


# Tools Used

- VHDL
- Xilinx Vivado
- Finite State Machine (FSM) Design Methodology

---

# Current Limitations

- The design has been validated **only through simulation**.
- No **physical FPGA implementation** was performed within the scope of this project.
- Some optional states may introduce **two clock-cycle delays** due to the simplified FSM structure.

---

# Future Work

Possible improvements for future development include:

- Implementing the design on a physical FPGA platform
- Optimizing FSM transitions to prevent entering unused states, thereby eliminating unnecessary clock cycles and improving timing efficiency.
- Expanding the testbench to cover **all operational scenarios**
- Integrating sensor inputs for real hardware interaction

---

# How to Run

1. Download the project ZIP file (vhdl‑washing‑machine‑controller.zip) from the repository.
2. Extract the ZIP to a desired location on your computer.
3. Open Xilinx Vivado and select **Open Project**.
4. Navigate to the extracted project folder and open the `.xpr` file.
5. You can now access all VHDL sources, testbenches, and IPs to simulate or modify the project.

---

# Documentation

The full academic thesis describing the design methodology, FSM architecture, and simulation results is included in the repository.

---

# Author

**Yasemin Kurt**

Electrical and Electronics Engineering Graduate
