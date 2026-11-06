# 4-Bit Universal Shift Register Simulation

## Objective

To design and verify the operation of a 4-bit Universal Shift Register using D Flip-Flops and 4:1 Multiplexers 

## Description

A Universal Shift Register is a sequential logic circuit that can perform four different operations: shift left, shift right, parallel load, and hold.

The circuit consists of four D Flip-Flops and four 4:1 Multiplexers. Each multiplexer selects one of four data inputs based on the select lines S1 and S0.

The selected data is transferred to the D Flip-Flops at the active clock edge. A common clock signal synchronizes all four flip-flops.

A Clear input is also provided to reset the register outputs.

## Inputs and Outputs

**Inputs:**
- S1, S0 – Mode selection inputs
- CLK – Clock input
- Clear – Reset input
- I3, I2, I1, I0 – Parallel data inputs
- Serial input for shift right
- Serial input for shift left

**Outputs:**
- A3, A2, A1, A0 – Parallel outputs

## Modes of Operation

| S1 | S0 | Operation |
|---|---|---|
| 0 | 0 | No change (Hold) |
| 0 | 1 | Shift Right |
| 1 | 0 | Shift Left |
| 1 | 1 | Parallel Load |

## Boolean Expressions

Let S1 and S0 be the selection inputs.

The multiplexer output equations are:

- **D3 = S1'S0' A3 + S1'S0 SR + S1S0' A2 + S1S0 I3**
- **D2 = S1'S0' A2 + S1'S0 A3 + S1S0' A1 + S1S0 I2**
- **D1 = S1'S0' A1 + S1'S0 A2 + S1S0' A0 + S1S0 I1**
- **D0 = S1'S0' A0 + S1'S0 A1 + S1S0' SL + S1S0 I0**

## Simulation

The circuit uses four 4:1 Multiplexers and four D Flip-Flops.

**Case 1: Hold (S1S0 = 00)**

- The previous data is retained.
- No shifting takes place.
- Register contents remain unchanged.

**Case 2: Shift Right (S1S0 = 01)**

- Data shifts towards the right.
- New serial data enters through the shift-right input.
- Each bit moves one position towards A0.

**Case 3: Shift Left (S1S0 = 10)**

- Data shifts towards the left.
- New serial data enters through the shift-left input.
- Each bit moves one position towards A3.

**Case 4: Parallel Load (S1S0 = 11)**

- All four input bits I3, I2, I1, and I0 are loaded simultaneously.
- The data appears at the parallel outputs after the active clock edge.
  
<img width="700" height="487" alt="image" src="https://github.com/user-attachments/assets/c68f7781-cc3b-4869-ad20-86045a96c9b1" />

## Truth Table

| S1 | S0 | Operation | Register Action |
|---|---|---|---|
| 0 | 0 | Hold | Retains previous data |
| 0 | 1 | Shift Right | Shifts data towards A0 |
| 1 | 0 | Shift Left | Shifts data towards A3 |
| 1 | 1 | Parallel Load | Loads I3, I2, I1, I0 |

## Shift Operation Table

**Shift Right**

| Clock | A3 | A2 | A1 | A0 |
|---|---|---|---|---|
| Initial | 1 | 0 | 1 | 1 |
| After 1 clock | SR | 1 | 0 | 1 |

**Shift Left**

| Clock | A3 | A2 | A1 | A0 |
|---|---|---|---|---|
| Initial | 1 | 0 | 1 | 1 |
| After 1 clock | 0 | 1 | 1 | SL |

## Uses

- Serial and parallel data transfer.
- Digital communication systems.
- Temporary data storage.
- Digital signal processing.
- Microprocessor and computer architecture.

## Observation

The operation of the Universal Shift Register depends on the selection inputs S1 and S0. The four 4:1 Multiplexers select the required data according to the selected mode. The D Flip-Flops store the selected data at the active clock edge. The circuit performs all four operations successfully.

## Conclusion

A 4-bit Universal Shift Register was designed and studied using four 4:1 Multiplexers and four D Flip-Flops.
