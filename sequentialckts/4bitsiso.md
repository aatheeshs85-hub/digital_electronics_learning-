# 4-Bit SISO Shift Register Simulation

## Objective

To design and verify the operation of a 4-bit Serial-In Serial-Out (SISO) Shift Register using D Flip-Flops in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A Serial-In Serial-Out (SISO) Shift Register is a sequential logic circuit used to store and transfer binary data one bit at a time.

The circuit consists of four D Flip-Flops connected in series with a common clock signal.

- Serial data is applied through the Din input.
- Four D Flip-Flops are connected in cascade.
- All flip-flops receive the same clock signal.
- Data shifts from one flip-flop to the next at every rising clock edge.
- The final serial output is obtained from Q0.

## Inputs and Outputs

**Inputs:** Din, CLK

**Output:** Q0 (Serial Output)

**Internal Connections:** Q3, Q2, Q1

## Boolean Expressions

The D Flip-Flop characteristic equation is:

**Q(next) = D**

For the four connected flip-flops:

- **D1 = Din**
- **D2 = Q3**
- **D3 = Q2**
- **D4 = Q1**

The final serial output is:

**Q0 = Output of the fourth D Flip-Flop**

Here, each flip-flop transfers its stored data to the next stage at the rising edge of the clock.

## Characteristic Table of D Flip-Flop

| D | Q (Next State) | Operation |
|---|---|---|
| 0 | 0 | Reset |
| 1 | 1 | Set |

## Simulation

The circuit uses four D Flip-Flops connected in series with a common clock.

Consider the serial input sequence: **1, 0, 1, 1**.

Assuming all flip-flops are initially reset to 0:

| Clock Pulse | Din | Q3 | Q2 | Q1 | Q0 (Output) |
|---|---|---|---|---|---|
| Initial | - | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |
| 2 | 0 | 0 | 1 | 0 | 0 |
| 3 | 1 | 1 | 0 | 1 | 0 |
| 4 | 1 | 1 | 1 | 0 | 1 |

The first input bit reaches the final output Q0 after four rising clock edges.
<img width="1917" height="1017" alt="image" src="https://github.com/user-attachments/assets/6a3b62e4-1df2-4227-8399-3f3ff4c76097" />

## Working Principle

1. Serial data is applied to the Din input.
2. At the first rising clock edge, the first D Flip-Flop stores the input bit.
3. At the second rising clock edge, the stored data moves to the second flip-flop.
4. The data continues shifting through the remaining flip-flops.
5. After four clock pulses, the first input bit reaches the final output Q0.
6. The remaining input bits follow the same shifting process.

## Uses

- Serial data transmission and reception.
- Temporary data storage.
- Serial communication systems.
- Microprocessor and microcontroller applications.

## Observation

The serial input data shifts through four D Flip-Flops at every rising clock edge. The data passes through each stage sequentially, and the final serial output is obtained at Q0. Q3, Q2 and Q1 are used as internal connections.

## Conclusion

A 4-bit SISO Shift Register was designed and simulated using four D Flip-Flops in Logisim Evolution v5.0.0. 
