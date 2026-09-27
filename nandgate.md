# NAND Gate Simulation

## Objective

To understand and verify the operation of a **NAND gate** using Logisim Evolution.

## Software Used

* Logisim Evolution v5.0.0

## Boolean Expression

**Y = (A · B)'**

## Truth Table

| A | B | Y |
| - | - | - |
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

## Simulation

The **NAND gate** was designed and tested using Logisim Evolution.
<img width="1917" height="1016" alt="Screenshot 2026-09-27 110121" src="https://github.com/user-attachments/assets/3c4aa5f1-68dc-4224-82d0-10c6ae7680ed" />


## Observation

The output of a NAND gate is the **complement of the AND gate output**.

* When **A = 0** and **B = 0**, the output is **Y = 1**.
* When **A = 0** and **B = 1**, the output is **Y = 1**.
* When **A = 1** and **B = 0**, the output is **Y = 1**.
* When **A = 1** and **B = 1**, the output is **Y = 0**.

In the shown simulation:

**A = 1**
**B = 1**
**Y = 0**

Therefore, the output device is **not activated**.

## Conclusion

The simulation successfully verified the **truth table and operation of the NAND gate**. The output was observed to be **LOW only when both inputs are HIGH**; for all other input combinations, the output is HIGH.
