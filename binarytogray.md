# Binary to Gray Code Converter

## Objective

To design and verify a **4-bit Binary to Gray Code Converter** using Logisim Evolution.

## Software Used

* Logisim Evolution v5.0.0

## Description

A **Binary to Gray Code Converter** is a combinational logic circuit that converts a binary number into its equivalent Gray code.

In Gray code, two consecutive numbers differ by only one bit. This reduces errors during transitions in digital systems.

The circuit consists of **4 input lines (B0, B1, B2, B3)** and **4 output lines (G0, G1, G2, G3)**.

---

## Boolean Expressions

The Boolean expressions for the converter are:

* **G0 = B0 ⊕ B1**
* **G1 = B1 ⊕ B2**
* **G2 = B2 ⊕ B3**
* **G3 = B3**

Here, **⊕ represents the XOR operation**.

---

## Simulation

For the shown Binary to Gray Code Converter simulation:

**Inputs:**

* B0 = 1
* B1 = 0
* B2 = 0
* B3 = 1

Using the Boolean expressions:

* G0 = B0 ⊕ B1 = 1 ⊕ 0 = **1**
* G1 = B1 ⊕ B2 = 0 ⊕ 0 = **0**
* G2 = B2 ⊕ B3 = 0 ⊕ 1 = **1**
* G3 = B3 = **1**

Therefore, the Gray code output is:

**G0G1G2G3 = 1011**

---
<img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/b60b164b-cf75-4ee6-8d23-3d29427988db" />

## Truth Table

| B0 | B1 | B2 | B3 | G0 | G1 | G2 | G3 |
| -- | -- | -- | -- | -- | -- | -- | -- |
| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| 0  | 0  | 0  | 1  | 0  | 0  | 1  | 1  |
| 0  | 0  | 1  | 0  | 0  | 1  | 1  | 0  |
| 0  | 0  | 1  | 1  | 0  | 1  | 0  | 1  |
| 0  | 1  | 0  | 0  | 1  | 1  | 0  | 0  |
| 0  | 1  | 0  | 1  | 1  | 1  | 1  | 1  |
| 0  | 1  | 1  | 0  | 1  | 0  | 1  | 0  |
| 0  | 1  | 1  | 1  | 1  | 0  | 0  | 1  |
| 1  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| 1  | 0  | 0  | 1  | 1  | 0  | 1  | 1  |
| 1  | 0  | 1  | 0  | 1  | 1  | 1  | 0  |
| 1  | 0  | 1  | 1  | 1  | 1  | 0  | 1  |
| 1  | 1  | 0  | 0  | 0  | 1  | 0  | 0  |
| 1  | 1  | 0  | 1  | 0  | 1  | 1  | 1  |
| 1  | 1  | 1  | 0  | 0  | 0  | 1  | 0  |
| 1  | 1  | 1  | 1  | 0  | 0  | 0  | 1  |

---

## Observation

* The XOR gates perform the required binary-to-Gray conversion.
* The most significant Gray code bit is directly connected to the corresponding binary bit.
* For the selected inputs B0 = 1, B1 = 0, B2 = 0, and B3 = 1, the output is **1011** when read in the displayed G0-to-G3 order.


## Uses of Binary to Gray Code Converter

1. Error reduction: Reduces errors during bit transitions in digital circuits.
2. Rotary encoders: Used to determine the position and rotation of motors and shafts.
3. Digital communication: Helps reduce errors when digital values change.
4. Analog-to-digital converters (ADCs): Gray coding can be used in certain ADC architectures to reduce errors during code transitions.

## Conclusion

The **4-bit Binary to Gray Code Converter** was successfully designed and simulated using Logisim Evolution. The simulation demonstrates the conversion of binary inputs into their corresponding Gray code outputs using XOR gates and a direct connection.
