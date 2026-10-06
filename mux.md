# Multiplexer (MUX) Simulation

## Objective

To design and verify the operation of **2×1 and 4×1 Multiplexers** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **Multiplexer (MUX)** is a combinational logic circuit that selects one input from multiple inputs and sends the selected input to a single output based on the select lines.

## 2×1 Multiplexer

A 2×1 MUX has:

- **2 Data Inputs:** I0, I1
- **1 Select Line:** S
- **1 Enable Input:** E
- **1 Output:** Y

### Boolean Expression

**Y = S̅I0 + SI1**

### Simulation

For the shown 2×1 MUX simulation:

**S = 1**

**I0 = 0**

**I1 = 0**

**E = 1**

Therefore:

**Y = 0**

Since **S = 1**, the MUX selects **I1**. As **I1 = 0**, the output is:

**Y = 0**

## 4×1 Multiplexer

A 4×1 MUX has:

- **4 Data Inputs:** I0, I1, I2, I3
- **2 Select Lines:** S1, S0
- **1 Output:** Y

### Boolean Expression

**Y = S1̅S0̅I0 + S1̅S0I1 + S1S0̅I2 + S1S0I3**

### Simulation

For the shown 4×1 MUX simulation:

**S1 = 1**

**S0 = 1**

**I0 = 0**

**I1 = 0**

**I2 = 0**

**I3 = 1**

Therefore:

**Y = 1**

Since **S1S0 = 11**, the MUX selects **I3**. As **I3 = 1**, the output is:

**Y = 1**
<img width="1907" height="1015" alt="image" src="https://github.com/user-attachments/assets/e4d4c703-8035-40f5-b197-4adeafaff7f6" />


## Truth Table

### 2×1 MUX

| S | Selected Input | Y |
|---|----------------|---|
| 0 | I0             | I0 |
| 1 | I1             | I1 |

### 4×1 MUX

| S1 | S0 | Selected Input | Y |
|----|----|----------------|---|
| 0  | 0  | I0             | I0 |
| 0  | 1  | I1             | I1 |
| 1  | 0  | I2             | I2 |
| 1  | 1  | I3             | I3 |

## Observation

The simulation verifies that a multiplexer selects one of the input signals according to the value of the select line or select lines.

For the 2×1 MUX, **S = 1** selects **I1**, producing **Y = 0**.

For the 4×1 MUX, **S1S0 = 11** selects **I3**, producing **Y = 1**.

## Conclusion

The **2×1 and 4×1 Multiplexers** were successfully designed and simulated using Logisim Evolution.
