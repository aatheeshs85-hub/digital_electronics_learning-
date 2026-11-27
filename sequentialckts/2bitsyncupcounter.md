# 2-BIT SYNCHRONOUS UP COUNTER

## 1. Introduction

A synchronous up counter is a sequential digital circuit that counts in an increasing binary sequence.

- It consists of two JK flip-flops.
- Both flip-flops receive the same external clock signal.
- The outputs change synchronously with the clock.
- A 2-bit counter has four possible states.
- It counts from 00 to 11 and then returns to 00.
- The counter is used to count clock pulses and divide frequencies.

## 2. Objective

To design and simulate a 2-bit synchronous up counter using JK flip-flops in Logisim Evolution.

## 3. Software Used

- Logisim Evolution v5.0.0

## 4. Components Used

- 2 JK Flip-Flops
- Clock
- Logic 1 input
- Output pins
- Connecting wires

## 5. Circuit Description

The circuit consists of two JK flip-flops connected in synchronous mode.

- The first flip-flop produces the least significant bit (Q1).
- The second flip-flop produces the most significant bit (Q2).
- Both flip-flops are connected to the same clock signal.
- The J and K inputs of the first flip-flop are connected to Logic 1.
- The J and K inputs of the second flip-flop are controlled by the output Q1.
- The first flip-flop toggles at every active clock edge.
- The second flip-flop toggles when Q1 is HIGH at the active clock edge.
- The outputs form a 2-bit binary counting sequence.

## 6. Boolean Expressions

### First Flip-Flop

J1 = 1

K1 = 1

The first flip-flop toggles at every active clock edge.

### Second Flip-Flop

J2 = Q1

K2 = Q1

The second flip-flop toggles when Q1 = 1.

### Next-State Equations

Q1(next) = NOT Q1

Q2(next) = Q2 XOR Q1

## 7. Truth Table

| Clock Pulse | Q2 | Q1 | Decimal |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 2 | 1 | 0 | 2 |
| 3 | 1 | 1 | 3 |
| 4 | 0 | 0 | 0 |

<img width="1917" height="1010" alt="image" src="https://github.com/user-attachments/assets/c3fd4042-b198-452f-849f-99f18a3a98c4" />

## 8. Counting Sequence

The counter follows the sequence:

00 → 01 → 10 → 11 → 00

## 9. Working Principle

1. Initially, the counter is in state 00.
2. When the clock pulse arrives, the first flip-flop toggles.
3. The output Q1 changes from 0 to 1.
4. During the next active clock edge, Q1 changes from 1 to 0.
5. Since Q1 was HIGH before that clock edge, the second flip-flop toggles.
6. The output becomes 10.
7. The counter continues through 11.
8. After reaching 11, the next clock pulse returns the counter to 00.
9. The counting process repeats continuously.

## 10. Simulation and Observation

- The circuit was designed using two JK flip-flops.
- A common clock signal was applied to both flip-flops.
- The outputs Q1 and Q2 were observed.
- The counter produced four binary states.
- Both flip-flops responded to the same clock signal.
- The circuit demonstrated synchronous up-counting operation.

## 11. Applications

- Digital counters
- Frequency divider circuits
- Digital clocks
- Sequence generators
- Timing circuits
- Control systems

## 12. Conclusion

A 2-bit synchronous up counter was designed and simulated using JK flip-flops in Logisim Evolution. Both flip-flops were connected to a common clock signal. The counter successfully generated the binary sequence 00, 01, 10, and 11, and then returned to 00. Thus, the synchronous up counter was successfully implemented.
