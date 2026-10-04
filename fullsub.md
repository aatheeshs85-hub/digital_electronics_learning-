# Full Subtractor Simulation

## Objective

To design and verify the operation of a **Full Subtractor** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **Full Subtractor** is a combinational logic circuit used to subtract two binary bits along with a borrow input. It has three inputs and two outputs.

### Inputs

- **A** – Minuend
- **B** – Subtrahend
- **Bin** – Borrow Input

### Outputs

- **D** – Difference
- **Bo** – Borrow Output

## Boolean Expressions

**D = A ⊕ B ⊕ Bin**

**Bo = A̅B + A̅Bin + BBin**

## Truth Table

| A | B | Bin | D | Bo |
|---|---|-----|---|----|
| 0 | 0 | 0   | 0 | 0  |
| 0 | 0 | 1   | 1 | 1  |
| 0 | 1 | 0   | 1 | 1  |
| 0 | 1 | 1   | 0 | 1  |
| 1 | 0 | 0   | 1 | 0  |
| 1 | 0 | 1   | 0 | 0  |
| 1 | 1 | 0   | 0 | 0  |
| 1 | 1 | 1   | 1 | 1  |

## Simulation

The Full Subtractor was designed and tested using **Logisim Evolution v5.0.0**.

For the shown simulation:

**A = 1**  
**B = 0**  
**Bin = 0**

Therefore:

**D = 1**

**Bo = 0**

<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/a535f784-f02d-43a4-a2cd-30334d7c0abf" />


## Observation

The circuit correctly performs the subtraction of three single-bit binary inputs. The **Difference (D)** output represents the result of the subtraction, while the **Borrow Output (Bo)** indicates whether a borrow is required.

## Conclusion

The Full Subtractor was successfully designed and simulated using Logisim Evolution.
