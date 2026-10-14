# Gray to Binary Converter

## Objective

To design and verify the operation of a **4-bit Gray to Binary Converter** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **Gray to Binary Converter** is a combinational logic circuit that converts a Gray code input into its equivalent binary number.

Gray code is a coding system in which two consecutive values differ by only one bit. The converter uses XOR gates to recover the original binary value from the Gray code.

The circuit consists of **4 input lines (G0, G1, G2, G3)** and **4 output lines (B0, B1, B2, B3)**.

---

## Boolean Expressions

The Boolean expressions used in the circuit are:

- **B0 = G0 ⊕ G1 ⊕ G2 ⊕ G3**
- **B1 = G1 ⊕ G2 ⊕ G3**
- **B2 = G2 ⊕ G3**
- **B3 = G3**

Here, **⊕ represents the XOR operation**.

---

## Simulation

For the shown Gray to Binary Converter simulation:

**Inputs:**

- G0 = 1
- G1 = 0
- G2 = 1
- G3 = 0

Using the Boolean expressions:

- B0 = 1 ⊕ 0 ⊕ 1 ⊕ 0 = **0**
- B1 = 0 ⊕ 1 ⊕ 0 = **1**
- B2 = 1 ⊕ 0 = **1**
- B3 = 0 = **0**

Therefore, the binary output is:

**B0B1B2B3 = 0110**
<img width="1917" height="1012" alt="image" src="https://github.com/user-attachments/assets/c25348f1-8d0e-4464-a602-6300edc33833" />

---

## Truth Table

| G0 | G1 | G2 | G3 | B0 | B1 | B2 | B3 |
|----|----|----|----|----|----|----|----|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 |
| 0 | 0 | 1 | 0 | 1 | 1 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 | 1 | 1 | 1 | 0 |
| 0 | 1 | 0 | 1 | 0 | 0 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 0 | 1 | 0 |
| 0 | 1 | 1 | 1 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 0 | 1 | 1 | 1 |
| 1 | 0 | 1 | 0 | 0 | 1 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 1 | 1 | 0 |
| 1 | 1 | 0 | 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 1 |

---

## Observation

- XOR gates are used to convert Gray code into binary code.
- The most significant binary bit is obtained directly from the corresponding Gray code bit.
- The remaining binary bits are obtained by successive XOR operations.
- The circuit produces the corresponding binary output for each Gray code input.

## Conclusion

The **4-bit Gray to Binary Converter** was successfully designed and simulated using Logisim Evolution. The simulation verifies that the Gray code inputs are correctly converted into their equivalent binary outputs.
