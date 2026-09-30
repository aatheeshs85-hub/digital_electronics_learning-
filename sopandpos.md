# Canonical SOP and POS Simulation

## Objective

To understand and verify the operation of Canonical Sum of Products (SOP) and Canonical Product of Sums (POS) using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Boolean Expression

### Canonical SOP Form

**Y(A,B,C) = Σm(0,2,3,6,7)**

**Y = A'B'C' + A'BC' + A'BC + ABC' + ABC**

### Canonical POS Form

**Y(A,B,C) = ΠM(1,4,5)**

**Y = (A+B+C')(A'+B+C)(A'+B+C')**

## Truth Table

| A | B | C | Y |
| - | - | - | - |
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

## Simulation

The Canonical SOP and POS circuits were designed and tested using Logisim Evolution.

### SOP Implementation

The SOP circuit was implemented using:

- NOT gates for complemented inputs
- AND gates for generating the required minterms
- OR gate for combining all the minterms

The selected minterms are:

**m(0,2,3,6,7)**

### POS Implementation

The POS circuit was implemented using:

- NOT gates for complemented inputs
- OR gates for generating the required maxterms
- AND gate for combining all the maxterms

The selected maxterms are:

**M(1,4,5)**

## Observation

The output of the Boolean function is HIGH (1) for minterms **0, 2, 3, 6, and 7**, and LOW (0) for minterms **1, 4, and 5**.

In the simulation:

**SOP Output = 1** for the selected minterm combinations.

**POS Output = 0** for the selected maxterm combinations.

<img width="1916" height="982" alt="image" src="https://github.com/user-attachments/assets/11fce2ea-6edb-4af2-8ffe-b3bc2fa61eb3" />


The circuits correctly implement their respective canonical forms.

## Conclusion

The simulation successfully verified the Canonical SOP and POS forms of the given Boolean function using Logisim Evolution. 

