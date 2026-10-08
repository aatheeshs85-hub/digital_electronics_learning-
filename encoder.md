# Encoder Simulation

## Objective

To design and verify the operation of **4:2 Encoder** and **8:3 Encoder** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

An **Encoder** is a combinational logic circuit that converts one active input from a set of input lines into a corresponding binary code at the output.

The number of output lines is determined by the number of input lines.

---

## 4:2 Encoder

A **4:2 Encoder** has:

- **4 Input Lines:** D0, D1, D2, D3
- **2 Output Lines:** X, Y

Only one input is normally active at a time.

### Boolean Expressions

**X = D2 + D3**

**Y = D1 + D3**

### Simulation

For the shown 4:2 Encoder simulation:

**D0 = 0**

**D1 = 0**

**D2 = 1**

**D3 = 0**

Therefore:

**X = 1**

**Y = 0**

Hence, the output is:

**XY = 10**

Since **D2 is active**, the encoder produces the binary code **10**.

### Truth Table

| D0 | D1 | D2 | D3 | X | Y |
|----|----|----|----|---|---|
| 1  | 0  | 0  | 0  | 0 | 0 |
| 0  | 1  | 0  | 0  | 0 | 1 |
| 0  | 0  | 1  | 0  | 1 | 0 |
| 0  | 0  | 0  | 1  | 1 | 1 |

---

## 8:3 Encoder

An **8:3 Encoder** has:

- **8 Input Lines:** D0 to D7
- **3 Output Lines:** X, Y, Z

The active input is converted into a corresponding 3-bit binary code.

### Boolean Expressions

**X = D4 + D5 + D6 + D7**

**Y = D2 + D3 + D6 + D7**

**Z = D1 + D3 + D5 + D7**

### Simulation

For the shown 8:3 Encoder simulation:

**D0 = 0**

**D1 = 0**

**D2 = 0**

**D3 = 0**

**D4 = 0**

**D5 = 1**

**D6 = 0**

**D7 = 0**

Therefore:

**X = 1**

**Y = 0**

**Z = 1**

Hence, the output is:

**XYZ = 101**

Since **D5 is active**, the encoder produces the binary code **101**.

### Truth Table

| Active Input | X | Y | Z |
|--------------|---|---|---|
| D0 | 0 | 0 | 0 |
| D1 | 0 | 0 | 1 |
| D2 | 0 | 1 | 0 |
| D3 | 0 | 1 | 1 |
| D4 | 1 | 0 | 0 |
| D5 | 1 | 0 | 1 |
| D6 | 1 | 1 | 0 |
| D7 | 1 | 1 | 1 |

<img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/ed114bba-8a8e-4605-ab65-923ad5f65ccc" />

---

## Observation

The encoder successfully converts the active input line into its corresponding binary code.

For the **4:2 Encoder**, when **D2 = 1**, the output obtained is:

**XY = 10**

For the **8:3 Encoder**, when **D5 = 1**, the output obtained is:

**XYZ = 101**

The simulated outputs match the expected encoder operation.

## Conclusion

The **4:2 Encoder and 8:3 Encoder** were successfully designed and simulated using Logisim Evolution. 
