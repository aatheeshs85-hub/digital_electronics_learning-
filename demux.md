# Demultiplexer (DEMUX) Simulation

## Objective

To design and verify the operation of **1:2 and 1:4 Demultiplexers** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **Demultiplexer (DEMUX)** is a combinational logic circuit that takes a single input and routes it to one of several output lines based on the select line or select lines.

It performs the reverse operation of a Multiplexer.

---

## 1:2 Demultiplexer

A 1:2 DEMUX has:

- **1 Data Input:** I
- **1 Select Line:** S0
- **2 Outputs:** Y0, Y1

### Boolean Expressions

**Y0 = I · S0̅**

**Y1 = I · S0**

### Simulation

For the shown 1:2 DEMUX simulation:

**I = 1**

**S0 = 0**

Therefore:

**Y0 = 1**

**Y1 = 0**

Since **S0 = 0**, the input is directed to **Y0**.

Hence:

**Y0 = 1**

**Y1 = 0**

### Truth Table

| S0 | I | Y0 | Y1 |
|----|---|----|----|
| 0  | 0 | 0  | 0  |
| 0  | 1 | 1  | 0  |
| 1  | 0 | 0  | 0  |
| 1  | 1 | 0  | 1  |

---

## 1:4 Demultiplexer

A 1:4 DEMUX has:

- **1 Data Input:** I
- **2 Select Lines:** S1, S0
- **4 Outputs:** Y0, Y1, Y2, Y3

### Boolean Expressions

**Y0 = I · S1̅ · S0̅**

**Y1 = I · S1̅ · S0**

**Y2 = I · S1 · S0̅**

**Y3 = I · S1 · S0**

### Simulation

For the shown 1:4 DEMUX simulation:

**I = 1**

**S1 = 1**

**S0 = 1**

Therefore:

**Y0 = 0**

**Y1 = 0**

**Y2 = 0**

**Y3 = 1**

Since **S1S0 = 11**, the input is directed to **Y3**.

Hence:

**Y3 = 1**

and all other outputs are **0**.

### Truth Table

| S1 | S0 | I | Y0 | Y1 | Y2 | Y3 |
|----|----|---|----|----|----|----|
| 0  | 0  | 1 | 1  | 0  | 0  | 0  |
| 0  | 1  | 1 | 0  | 1  | 0  | 0  |
| 1  | 0  | 1 | 0  | 0  | 1  | 0  |
| 1  | 1  | 1 | 0  | 0  | 0  | 1  |

If **I = 0**, all outputs are 0 for every select-line combination.
<img width="1917" height="1007" alt="image" src="https://github.com/user-attachments/assets/ff99efcd-8a44-4942-a003-5f55ec689485" />

---

## Observation

The DEMUX successfully routes a single input signal to one of the available output lines according to the select lines.

For the 1:2 DEMUX, **S0 = 0** selects **Y0**.

For the 1:4 DEMUX, **S1S0 = 11** selects **Y3**.

Only the selected output receives the input signal, while the remaining outputs remain LOW.

## Conclusion

The **1:2 and 1:4 Demultiplexers** were successfully designed and simulated using Logisim Evolution. 
