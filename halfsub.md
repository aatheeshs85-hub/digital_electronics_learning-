# Half Subtractor Simulation

## Objective

To design and verify the operation of a **Half Subtractor** using digital logic gates.

## Software Used

- Digital Logic Simulator

## Description

A **Half Subtractor** is a combinational logic circuit used to subtract one single-bit binary input from another. It has two inputs and two outputs.

### Inputs

- **A** – Minuend
- **B** – Subtrahend

### Outputs

- **Difference**
- **Borrow**

## Boolean Expressions

**Difference = A ⊕ B**

**Borrow = A̅ · B**

## Truth Table

| A | B | Difference | Borrow |
|---|---|------------|--------|
| 0 | 0 | 0          | 0      |
| 0 | 1 | 1          | 1      |
| 1 | 0 | 1          | 0      |
| 1 | 1 | 0          | 0      |


## Simulation

The Half Subtractor circuit was designed and tested using a digital logic simulator.

For the shown simulation:

**A = 0**

**B = 1**

Therefore:

**Difference = 1**

**Borrow = 1**
<img width="997" height="670" alt="image" src="https://github.com/user-attachments/assets/cfb45d03-f082-44cc-9794-370dfbde4deb" />


## Observation

When **A = 0** and **B = 1**, the circuit produces **Difference = 1** and **Borrow = 1**.

The simulation output matches the expected Half Subtractor truth table.

## Conclusion

The Half Subtractor was successfully designed and simulated. 
