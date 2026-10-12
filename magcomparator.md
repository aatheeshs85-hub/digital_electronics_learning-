# 2-Bit Magnitude Comparator Simulation

## Objective

To design and verify the operation of a **2-Bit Magnitude Comparator** using Logisim Evolution.

## Software Used

* Logisim Evolution v5.0.0

## Description

A **Magnitude Comparator** is a combinational logic circuit used to compare two binary numbers and determine whether the first number is greater than, less than, or equal to the second number.

A 2-bit magnitude comparator compares two 2-bit binary numbers, A and B.

* **Input A:** A1, A0
* **Input B:** B1, B0
* **Output 1:** A = B
* **Output 2:** A > B
* **Output 3:** A < B

The circuit produces three outputs, and only one output is HIGH for any valid comparison.

---

## 2-Bit Magnitude Comparator

### Boolean Expressions

**Equality Output (A = B)**

`A = B = (A1 XNOR B1) · (A0 XNOR B0)`

**Greater Than Output (A > B)**

`A > B = A1B1' + (A1 XNOR B1)A0B0'`

**Less Than Output (A < B)**

`A < B = A1'B1 + (A1 XNOR B1)A0'B0`

Here, `'` represents NOT, `·` represents AND, and `+` represents OR.

### Simulation

For the shown 2-Bit Magnitude Comparator simulation:

**A1 = 1**

**A0 = 1**

**B1 = 0**

**B0 = 1**

Therefore:

**A = 11₂ = 3**

**B = 01₂ = 1**

Since A is greater than B:

* **A = B = 0**
* **A > B = 1**
* **A < B = 0**

Hence, the output indicates:

**A > B**
<img width="1917" height="1017" alt="image" src="https://github.com/user-attachments/assets/af828baf-ba3d-4310-972f-29f3e588bb47" />

### Truth Table

| A1 | A0 | B1 | B0 | A = B | A > B | A < B |
| -- | -- | -- | -- | ----- | ----- | ----- |
| 0  | 0  | 0  | 0  | 1     | 0     | 0     |
| 0  | 0  | 0  | 1  | 0     | 0     | 1     |
| 0  | 0  | 1  | 0  | 0     | 0     | 1     |
| 0  | 0  | 1  | 1  | 0     | 0     | 1     |
| 0  | 1  | 0  | 0  | 0     | 1     | 0     |
| 0  | 1  | 0  | 1  | 1     | 0     | 0     |
| 0  | 1  | 1  | 0  | 0     | 0     | 1     |
| 0  | 1  | 1  | 1  | 0     | 0     | 1     |
| 1  | 0  | 0  | 0  | 0     | 1     | 0     |
| 1  | 0  | 0  | 1  | 0     | 1     | 0     |
| 1  | 0  | 1  | 0  | 0     | 0     | 1     |
| 1  | 0  | 1  | 1  | 0     | 0     | 1     |
| 1  | 1  | 0  | 0  | 0     | 1     | 0     |
| 1  | 1  | 0  | 1  | 0     | 1     | 0     |
| 1  | 1  | 1  | 0  | 0     | 1     | 0     |
| 1  | 1  | 1  | 1  | 1     | 0     | 0     |

---

## Observation

The magnitude comparator successfully compares two 2-bit binary numbers and generates the appropriate output.

For the given simulation:

**A = 11₂ = 3**

**B = 01₂ = 1**

The output obtained is:

**A = B = 0**

**A > B = 1**

**A < B = 0**

The simulated outputs match the expected comparator operation.

## Conclusion

The **2-Bit Magnitude Comparator** was successfully designed and simulated using Logisim Evolution. The circuit compares two 2-bit binary numbers and correctly indicates whether A is equal to, greater than, or less than B.
