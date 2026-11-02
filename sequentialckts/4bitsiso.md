# 4-Bit SISO Shift Register Simulation

## Objective

To design and verify the operation of a 4-bit Serial-In Serial-Out (SISO) Shift Register using D Flip-Flops in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A Serial-In Serial-Out (SISO) Shift Register is a sequential logic circuit used to store and transfer binary data serially.

It consists of four D Flip-Flops connected in series with a common clock signal.

- Serial data is applied through the Din input.
- Each D Flip-Flop stores one bit of data.
- Data shifts from one flip-flop to the next at every rising clock edge.
- The final serial output is obtained from Q0.

## Inputs and Outputs

**Inputs:** Din, CLK

**Output:** Q0 (Serial Output)

**Internal Connections:** Q3, Q2, Q1

## Boolean Expressions

At every active rising clock edge:

- **Q3 = Din**
- **Q2 = Q3 (Previous State)**
- **Q1 = Q2 (Previous State)**
- **Q0 = Q1 (Previous State)**

Each flip-flop transfers its stored data to the next flip-flop at the active clock edge.

## Simulation

The circuit uses four D Flip-Flops connected in series.

Consider the serial input sequence: 1, 0, 1, 1.

Assuming all flip-flops are initially reset to 0:

<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/7e139049-3c30-49f6-86cc-9cbb975bc691" />

| Clock Pulse | Din | Q3 | Q2 | Q1 | Q0 (Output) |
|---|---|---|---|---|---|
| Initial | - | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |
| 2 | 0 | 0 | 1 | 0 | 0 |
| 3 | 1 | 1 | 0 | 1 | 0 |
| 4 | 1 | 1 | 1 | 0 | 1 |

The first input bit reaches the final output Q0 after four rising clock edges.

## Timing Response

<img width="980" height="295" alt="image" src="https://github.com/user-attachments/assets/2dc179f8-38e1-4944-9c8c-5b4732b457c1" />

## Working Principle

1. Serial data is applied to the Din input.
2. At the first rising clock edge, the first D Flip-Flop stores the input bit.
3. At the next clock edge, the stored bit moves to the second flip-flop.
4. The data continues shifting through the third and fourth flip-flops.
5. After four clock pulses, the first input bit reaches the final serial output Q0.
6. Subsequent input bits also reach Q0 in the same serial manner.

## Uses

- Serial data transmission and reception.
- Temporary data storage.
- Digital communication systems.
- Data transfer circuits.

## Observation

The serial input data shifts through four D Flip-Flops with every rising clock edge. The data appears at the final output Q0 after passing through all four flip-flops. Q3, Q2 and Q1 act as internal intermediate stages.

## Conclusion

A 4-bit SISO Shift Register was designed and simulated using four D Flip-Flops in Logisim Evolution v5.0.0. 
