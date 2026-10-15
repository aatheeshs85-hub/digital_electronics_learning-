# BCD to Excess-3 Converter

## Objective

To design and verify the operation of a **BCD to Excess-3 Code Converter** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **BCD to Excess-3 Converter** is a combinational logic circuit that converts a 4-bit Binary Coded Decimal (BCD) number into its corresponding Excess-3 code.

Excess-3 is a non-weighted, self-complementing code. It is obtained by adding **0011 (decimal 3)** to a valid BCD input.

The circuit consists of four input lines (**B3, B2, B1, B0**) and four output lines (**E3, E2, E1, E0**).

---

## Boolean Expressions

The Boolean expressions for the BCD to Excess-3 converter are:

- **E3 = B3 + B2B1 + B2B0**
- **E2 = B2'B1' + B2'B0' + B2B1B0**
- **E1 = B1 ⊕ B0**
- **E0 = B0'**

---

## Simulation

For the shown simulation:

**Input values:**

- B3 = 0
- B2 = 1
- B1 = 1
- B0 = 1

The BCD input is **0111**, representing decimal 7.

Adding 3 to the input:

**0111 + 0011 = 1010**

Therefore, the expected Excess-3 output is:

- E3 = 1
- E2 = 0
- E1 = 1
- E0 = 0

**Final output: E3E2E1E0 = 1010**

The output represents the Excess-3 code for decimal 7.
<img width="1917" height="1011" alt="image" src="https://github.com/user-attachments/assets/d62b48bb-2832-43ca-a570-d16e66de0677" />

---

## Truth Table

| Decimal | B3 | B2 | B1 | B0 | E3 | E2 | E1 | E0 |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 0 |
| 2 | 0 | 0 | 1 | 0 | 0 | 1 | 0 | 1 |
| 3 | 0 | 0 | 1 | 1 | 0 | 1 | 1 | 0 |
| 4 | 0 | 1 | 0 | 0 | 0 | 1 | 1 | 1 |
| 5 | 0 | 1 | 0 | 1 | 1 | 0 | 0 | 0 |
| 6 | 0 | 1 | 1 | 0 | 1 | 0 | 0 | 1 |
| 7 | 0 | 1 | 1 | 1 | 1 | 0 | 1 | 0 |
| 8 | 1 | 0 | 0 | 0 | 1 | 0 | 1 | 1 |
| 9 | 1 | 0 | 0 | 1 | 1 | 1 | 0 | 0 |

---

## Uses of BCD to Excess-3 Converter

1. **Digital arithmetic circuits:** Used in decimal arithmetic systems that operate with Excess-3 representation.
2. **Calculators:** Can be used in decimal calculation circuits that require conversion between BCD and Excess-3 codes.
3. **Digital electronics:** Used to demonstrate and implement code conversion in combinational logic circuits.
4. **Complement arithmetic:** The self-complementing property of Excess-3 can simplify 9's-complement operations in certain decimal arithmetic designs.

---

## Observation

- The circuit converts valid BCD inputs into their corresponding Excess-3 codes.
- The conversion is performed by adding binary `0011` to each valid BCD digit.
- For the input **0111**, the expected output is **1010**.
- The truth table verifies the conversion for decimal digits 0 through 9.
- Inputs from `1010` to `1111` are invalid BCD digits and are not included in the truth table.

---

## Conclusion

The **BCD to Excess-3 Converter** was designed and simulated using Logisim Evolution v5.0.0. 
