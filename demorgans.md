# De Morgan's Theorems Simulation

## Objective

To understand and verify **De Morgan's Theorems** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Boolean Expressions

### First De Morgan's Theorem

**Y = (A + B)'= A̅ · B̅**

### Second De Morgan's Theorem

**Y = (A · B)'= A̅ + B̅**

## Truth Table

| A | B | (A + B)'| A̅ · B̅ | (A · B)'| A̅ + B̅ |
| - | - | - | - | - | - |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |

## Simulation

The **first and second De Morgan's Theorems** were designed and tested using Logisim Evolution.

First theorem
<img width="1581" height="887" alt="Screenshot 2026-09-29 193210" src="https://github.com/user-attachments/assets/61f0979f-48af-45ea-b790-69c180b496a1" />


Second theorem
<img width="1616" height="902" alt="Screenshot 2026-09-29 193535" src="https://github.com/user-attachments/assets/8da827d7-89fc-49b0-b0d9-ec53665b6856" />


## Observation

### First De Morgan's Theorem

The first circuit consists of an **OR gate followed by a NOT gate**, which produces:

**Y = (A + B)'**

The equivalent circuit consists of **NOT gates connected to both inputs followed by an AND gate**, which produces:

**Y = A̅ · B̅**

Therefore:

**(A + B)'= A̅ · B̅**

### Second De Morgan's Theorem

The second circuit consists of an **AND gate followed by a NOT gate**, which produces:

**Y = (A · B)'**

The equivalent circuit consists of **NOT gates connected to both inputs followed by an OR gate**, which produces:

**Y = A̅ + B̅**

Therefore:

**(A · B)'= A̅ + B̅**

For example, when:

**A = 1**  
**B = 0**

First theorem:

**(1 + 0)'= 0**

**0'· 1'= 0 · 1 = 0**

Second theorem:

**(1 · 0)'= 1**

**0 + 1 = 1**

Thus, the outputs of the equivalent circuits are the same.

## Applications

De Morgan's Theorems are commonly used in:

- **Logic Circuit Simplification** – Used to simplify Boolean expressions.
- **Digital Circuit Design** – Used to transform and optimize logic circuits.
- **NAND/NOR Implementation** – Helps in implementing circuits using universal gates.
- **Boolean Algebra** – Used for simplifying logical expressions.
- **Combinational Circuits** – Used in the design of digital logic circuits.

## Conclusion

The simulation successfully verified **both De Morgan's Theorems**. The outputs of the equivalent circuits were found to be the same for all possible combinations of inputs.
