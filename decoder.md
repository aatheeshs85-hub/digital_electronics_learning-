# Decoder Simulation

## Objective

To design and verify the operation of **2:4 Decoder** and **3:8 Decoder** using Logisim Evolution.

## Software Used

* Logisim Evolution v5.0.0

## Description

A **Decoder** is a combinational logic circuit that converts binary input data into a specific output line. For each valid input combination, one output line becomes active.

The number of output lines is determined by the number of input lines.

---

## 2:4 Decoder

A **2:4 Decoder** has:

* **2 Input Lines:** X, Y
* **1 Enable Input:** E
* **4 Output Lines:** D0, D1, D2, D3

The enable input controls the operation of the decoder. When E = 1, the decoder operates normally. When E = 0, all outputs remain 0.

### Boolean Expressions

**D0 = E · X̅ · Y̅**

**D1 = E · X̅ · Y**

**D2 = E · X · Y̅**

**D3 = E · X · Y**

### Simulation

For the shown 2:4 Decoder simulation:

**E = 1**

**X = 1**

**Y = 0**

Therefore:

**D0 = 0**

**D1 = 0**

**D2 = 1**

**D3 = 0**

Hence, the active output is:

**D2 = 1**

Since the input combination is **XY = 10**, the decoder activates output **D2**.

### Truth Table

| E | X | Y | D0 | D1 | D2 | D3 |
| - | - | - | -- | -- | -- | -- |
| 0 | X | X | 0  | 0  | 0  | 0  |
| 1 | 0 | 0 | 1  | 0  | 0  | 0  |
| 1 | 0 | 1 | 0  | 1  | 0  | 0  |
| 1 | 1 | 0 | 0  | 0  | 1  | 0  |
| 1 | 1 | 1 | 0  | 0  | 0  | 1  |

---

## 3:8 Decoder

A **3:8 Decoder** has:

* **3 Input Lines:** X, Y, Z
* **8 Output Lines:** D0, D1, D2, D3, D4, D5, D6, D7

The 3-bit binary input is converted into one active output among eight output lines.

### Boolean Expressions

**D0 = X̅ · Y̅ · Z̅**

**D1 = X̅ · Y̅ · Z**

**D2 = X̅ · Y · Z̅**

**D3 = X̅ · Y · Z**

**D4 = X · Y̅ · Z̅**

**D5 = X · Y̅ · Z**

**D6 = X · Y · Z̅**

**D7 = X · Y · Z**

### Simulation

For the shown 3:8 Decoder simulation:

**X = 1**

**Y = 1**

**Z = 0**

Therefore:

**D0 = 0**

**D1 = 0**

**D2 = 0**

**D3 = 0**

**D4 = 0**

**D5 = 0**

**D6 = 1**

**D7 = 0**

Hence, the active output is:

**D6 = 1**

Since the input combination is **XYZ = 110**, the decoder activates output **D6**.

### Truth Table

| X | Y | Z | Active Output |
| - | - | - | ------------- |
| 0 | 0 | 0 | D0 = 1        |
| 0 | 0 | 1 | D1 = 1        |
| 0 | 1 | 0 | D2 = 1        |
| 0 | 1 | 1 | D3 = 1        |
| 1 | 0 | 0 | D4 = 1        |
| 1 | 0 | 1 | D5 = 1        |
| 1 | 1 | 0 | D6 = 1        |
| 1 | 1 | 1 | D7 = 1        |

---

## Observation

The decoders successfully convert binary input combinations into their corresponding active output lines.

For the **2:4 Decoder**, when **E = 1, X = 1, Y = 0**, the active output is:

**D2 = 1**

For the **3:8 Decoder**, when **X = 1, Y = 1, Z = 0**, the active output is:

**D6 = 1**

<img width="1917" height="1015" alt="image" src="https://github.com/user-attachments/assets/7d326d3d-5453-445e-8b92-fc7826ad908c" />


## Conclusion

The **2:4 Decoder and 3:8 Decoder** were successfully designed and simulated using Logisim Evolution. 
