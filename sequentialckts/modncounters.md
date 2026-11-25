# MOD-6 COUNTER USING MOD-8 COUNTER

## 1. Introduction

A MOD-6 counter is a digital counter that counts six states, from 0 to 5, and then returns to 0.

- A 3-bit counter is required to represent six different states.
- A MOD-8 counter normally counts from 000 to 111 (0 to 7).
- By adding a reset circuit, the MOD-8 counter can be converted into a MOD-6 counter.
- The counter uses three JK flip-flops to store the binary count.
- The reset circuit detects the count 110 (decimal 6) and clears the counter to 000.
- The counter operates using clock pulses.

## 2. Objective

To design and simulate a MOD-6 counter using a MOD-8 counter in Logisim Evolution.

## 3. Software Used

- Logisim Evolution v5.0.0

## 4. Components Used

- 3 JK Flip-Flops
- AND Gate
- NOT Gates
- Clock
- Logic 1 input
- Output pins
- Connecting wires

## 5. Circuit Description

The circuit consists of three JK flip-flops connected to form a 3-bit asynchronous counter.

- The first flip-flop produces the least significant bit (QA).
- The second flip-flop produces the middle bit (QB).
- The third flip-flop produces the most significant bit (QC).
- The JK inputs are connected to Logic 1 so that each flip-flop toggles when triggered.
- The output of the first flip-flop is connected to the clock input of the second flip-flop.
- The output of the second flip-flop is connected to the clock input of the third flip-flop.
- The outputs QA, QB, and QC are connected to a reset detection circuit.
- When the counter reaches 110, the reset circuit clears all flip-flops.
- The counter then starts counting again from 000.

## 6. Boolean Expressions

### JK Flip-Flop Toggle Condition

J = 1

K = 1

When J = K = 1, the JK flip-flop toggles its output at the active clock edge.

### Counter Reset Logic

The counter resets when the output becomes 110.

Reset condition:

QC = 1

QB = 1

QA = 0

The reset detection equation is:

RESET = QC · QB · QA'

Where:

- QC = Most significant bit
- QB = Middle bit
- QA = Least significant bit
- QA' = Complement of QA

The reset condition can also be written as:

RESET = QC AND QB AND NOT QA

## 7. Counting Sequence

The MOD-6 counter follows the sequence:

000 → 001 → 010 → 011 → 100 → 101 → 000

The counter does not continue to 110 or 111 during normal operation.

## 8. Truth Table

| Clock Pulse | QC | QB | QA | Decimal |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 |
| 2 | 0 | 1 | 0 | 2 |
| 3 | 0 | 1 | 1 | 3 |
| 4 | 1 | 0 | 0 | 4 |
| 5 | 1 | 0 | 1 | 5 |
| 6 | 0 | 0 | 0 | Reset |

<img width="1917" height="1018" alt="Screenshot 2026-11-25 195540" src="https://github.com/user-attachments/assets/b8a94abf-966a-4e14-8dd1-a2c6e445cdab" />


## 9. Working Principle

1. Initially, the counter is in the state 000.
2. When the clock pulses are applied, QA toggles.
3. When QA changes from 1 to 0, QB toggles.
4. When QB changes from 1 to 0, QC toggles.
5. The counter progresses through the binary states from 000 to 101.
6. When the counter reaches 110, the reset logic detects the state.
7. The reset signal clears the flip-flops to 000.
8. The counting process repeats continuously.

## 10. Simulation and Observation

- The circuit was designed using JK flip-flops and logic gates.
- The clock was applied to the counter.
- The outputs QA, QB, and QC were observed.
- The counter produced six valid states.
- The reset logic returned the counter to 000 after reaching 110.
- The circuit demonstrated MOD-6 counting operation.

## 11. Applications

- Digital clocks
- Frequency division circuits
- Sequence generators
- Digital control systems
- Timing circuits
- Event counting systems

## 12. Conclusion

A MOD-6 counter was designed using a MOD-8 counter in Logisim Evolution. The circuit uses three JK flip-flops and a reset detection logic circuit. By detecting the state 110 and resetting the counter, the circuit counts from 0 to 5 and repeats. Thus, the MOD-8 counter is successfully converted into a MOD-6 counter.
