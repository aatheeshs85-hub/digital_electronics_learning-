# 4-Bit PISO Shift Register Simulation

## Objective

To design and verify the operation of a 4-bit Parallel-In Serial-Out (PISO) Shift Register using D Flip-Flops and logic gates in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A Parallel-In Serial-Out (PISO) Shift Register is a sequential logic circuit that accepts multiple input bits simultaneously and transfers them serially, one bit at a time.

The circuit consists of four D Flip-Flops, AND gates and OR gates.

- Four parallel input bits are applied simultaneously through B0, B1, B2 and B3.
- A common clock signal is connected to all four flip-flops.
- The SHIFT/LOAD control signal selects the operating mode.
- In Load mode, all four input bits are stored in the register.
- In Shift mode, the stored bits move towards the final output.
- The serial output is obtained from Q3.

## Inputs and Outputs

**Inputs:** B0, B1, B2, B3, SHIFT/LOAD', CLK

**Output:** Q3 (Serial Output)

**Internal Connections:** Q0, Q1, Q2

## Boolean Expressions

The circuit uses AND and OR gates to implement the shift/load selection.

Let L represent Load and S represent Shift.

- **D0 = B0**
- **D1 = (L · B1) + (S · Q0)**
- **D2 = (L · B2) + (S · Q1)**
- **D3 = (L · B3) + (S · Q2)**

The D Flip-Flops store the selected data at the rising edge of the clock.

## Mode Selection Table

| Load (L) | Shift (S) | Operation |
|---|---|---|
| 1 | 0 | Parallel Load |
| 0 | 1 | Shift |
 
## Characteristic Table of D Flip-Flop

| D | Q (Next State) | Operation |
|---|---|---|
| 0 | 0 | Store 0 |
| 1 | 1 | Store 1 |

## Simulation

The circuit uses four D Flip-Flops connected with AND-OR logic gates.

Consider the parallel input combination:

- B3 = 1
- B2 = 0
- B1 = 1
- B0 = 1

During the Load operation, all four bits are stored simultaneously.

The register contents are:

**Q3 Q2 Q1 Q0 = 1011**

During the Shift operation, the bits move towards the serial output Q3.

| Clock Pulse | Q3 | Q2 | Q1 | Q0 | Serial Output |
|---|---|---|---|---|---|
| Load | 1 | 0 | 1 | 1 | 1 |
| Shift 1 | 0 | 1 | 1 | 1 | 0 |
| Shift 2 | 1 | 1 | 1 | 1 | 1 |
| Shift 3 | 1 | 1 | 1 | 1 | 1 |
The serial output is obtained one bit at a time from Q3.

<img width="1917" height="1016" alt="image" src="https://github.com/user-attachments/assets/774caf8a-b46e-4cd5-85ac-a8ced9532ace" />

## Working Principle

1. Four parallel input bits are applied through B0, B1, B2 and B3.
2. The Load mode is selected to store all four bits simultaneously.
3. At the rising edge of the clock, the D Flip-Flops capture the selected data.
4. The Shift mode is selected to transfer the stored bits towards the next flip-flop.
5. Each clock pulse shifts the data towards the final output Q3.
6. The stored data is obtained serially through Q3.

## Uses

- Parallel-to-serial data conversion.
- Digital communication systems.
- Data transfer between digital circuits.
- Microprocessor and microcontroller applications.

## Observation

The parallel input data is stored simultaneously during Load mode. During Shift mode, the stored bits move through the flip-flops with every rising clock edge. The serial data is obtained through Q3.

## Conclusion

A 4-bit PISO Shift Register was designed and simulated using D Flip-Flops, AND gates and OR gates in Logisim Evolution v5.0.0. 
