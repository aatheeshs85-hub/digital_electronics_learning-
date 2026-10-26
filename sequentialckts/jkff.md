# JK Flip-Flop Using NAND Gates

## 📌 Project Overview

This project demonstrates the design and simulation of a **JK Flip-Flop using NAND gates** in Logisim Evolution. A JK flip-flop is a sequential logic circuit that stores one bit of data and operates according to the inputs J, K, and CLK.

The circuit produces two complementary outputs, Q and Q̅.

## 🎯 Objectives

- To understand the working principle of a JK flip-flop.
- To design a JK circuit using NAND gates.
- To simulate the circuit using Logisim Evolution.
- To verify the output using the JK flip-flop truth table.

## 🛠️ Software Used

- **Logisim Evolution** – Digital logic circuit design and simulation.

## 🔌 Circuit Diagram

The following diagram shows the logical structure of a NAND-based, clock-enabled JK latch.

<img width="1100" height="608" alt="image" src="https://github.com/user-attachments/assets/7ecfcbc1-b51c-4be0-8a6d-8aad1f63bc6c" />


**Note:** The feedback connections are essential. Q feeds the lower input NAND gate, while Q̅ feeds the upper input NAND gate. The two output NAND gates form a cross-coupled latch.

## 📊 Truth Table

| J | K | Clock condition | Operation | Next Q |
|---|---|---|---|---|
| 0 | 0 | Active | Hold | Previous Q |
| 0 | 1 | Active | Reset | 0 |
| 1 | 0 | Active | Set | 1 |
| 1 | 1 | Active | Toggle | Q̅ (previous) |

## ⚙️ Working Principle

1. **Hold (J = 0, K = 0):** The circuit retains its previous state.
2. **Reset (J = 0, K = 1):** The output Q becomes 0.
3. **Set (J = 1, K = 0):** The output Q becomes 1.
4. **Toggle (J = 1, K = 1):** The output changes to its opposite state when the clock is active.

The NAND gates at the input generate the control signals, while the cross-coupled NAND gates store the output state.

## 🧪 Simulation Procedure

1. Open Logisim Evolution.
2. Place four NAND gates on the workspace.
3. Add input pins for J, K, and CLK.
4. Connect the NAND gates according to the circuit diagram.
5. Add output pins for Q and Q̅.
6. Change the input combinations and observe the outputs.
7. Compare the simulated results with the truth table.

## ✅ Expected Results

- The circuit stores one bit of information.
- Q and Q̅ are complementary during valid stable operation.
- The output behavior follows the JK truth table when the circuit operates correctly.

## ⚠️ Important Note

This four-NAND arrangement is a **clock-enabled JK latch**, not a true edge-triggered JK flip-flop. When J = K = 1 and the clock remains HIGH, repeated toggling or oscillation may occur. A master-slave or edge-triggered design is required to avoid this race-around problem.

## 📚 Applications

- Digital memory circuits
- Counters and frequency dividers
- Registers and control circuits
- Sequential logic systems

## 🏁 Conclusion

The JK flip-flop demonstrates how NAND gates can be combined with feedback to create a one-bit storage circuit. Logisim Evolution helps visualize the circuit behavior and verify its operation using different input combinations.

---

**Project Type:** Digital Electronics / Sequential Logic  
**Tool:** Logisim Evolution  
**Main Components:** NAND Gates, Input Pins, Clock, Output Pins
