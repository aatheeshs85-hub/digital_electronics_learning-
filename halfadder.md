# Half Adder Simulation

## Objective

To design and verify the operation of a **Half Adder** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **Half Adder** is a combinational logic circuit used to add two single-bit binary numbers. It produces two outputs:

- **SUM**
- **CARRY**

The circuit consists of an **XOR gate** for the SUM output and an **AND gate** for the CARRY output.

## Boolean Expressions

**SUM = A ⊕ B**

**CARRY = A · B**

## Truth Table

| A | B | SUM | CARRY |
|---|---|-----|-------|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |

## Circuit

The Half Adder circuit is implemented using:

- XOR Gate → SUM
- AND Gate → CARRY

## Simulation

For the shown simulation:

**A = 0**  
**B = 1**

Therefore:

**SUM = 1**  
**CARRY = 0**

<img width="1917" height="1021" alt="image" src="https://github.com/user-attachments/assets/0a6a385d-bd98-453a-9f38-d2ceb554c3c7" />

## Observation

The circuit produces the correct SUM and CARRY outputs for the given input combinations. The simulation output matches the Half Adder truth table.

## Conclusion

The Half Adder was successfully designed and simulated in Logisim Evolution. The results verify that the circuit performs binary addition of two single-bit inputs correctly.
