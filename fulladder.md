# Full Adder Simulation

## Objective

To design and verify the operation of a **Full Adder** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **Full Adder** is a combinational logic circuit used to add three single-bit binary inputs. It produces two outputs:

- **SUM**
- **CARRY**

The three inputs are **A**, **B**, and **Cin (Carry Input)**.

## Boolean Expressions

**SUM = A ⊕ B ⊕ Cin**

**CARRY = AB + BCin + ACin**

## Truth Table

| A | B | Cin | SUM | CARRY |
|---|---|-----|-----|-------|
| 0 | 0 | 0   | 0   | 0     |
| 0 | 0 | 1   | 1   | 0     |
| 0 | 1 | 0   | 1   | 0     |
| 0 | 1 | 1   | 0   | 1     |
| 1 | 0 | 0   | 1   | 0     |
| 1 | 0 | 1   | 0   | 1     |
| 1 | 1 | 0   | 0   | 1     |
| 1 | 1 | 1   | 1   | 1     |

## Simulation

The Full Adder was designed and tested using **Logisim Evolution v5.0.0**.

For the shown simulation:

**A = 1**  
**B = 0**  
**Cin = 1**

Therefore:

**SUM = 0**  
**CARRY = 1**

<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/fc27c572-e727-4fed-9b92-2922f50d2f17" />

## Observation

The circuit correctly performs the addition of three single-bit binary inputs. The SUM output represents the result bit, while the CARRY output represents the carry generated during the addition.

## Conclusion

The Full Adder was successfully designed and simulated using Logisim Evolution.
