# 3-Bit Asynchronous UP/DOWN Counter

## Objective
To design and simulate a 3-bit asynchronous UP/DOWN counter using JK flip-flops and XOR gates in Logisim Evolution. The circuit counts in both ascending and descending binary sequences depending on the mode control input.

## Software Used
- Logisim Evolution v5.0.0

## Description
A 3-bit asynchronous UP/DOWN counter is a sequential digital circuit that can count in both increasing and decreasing binary order.

- The circuit consists of three JK flip-flops connected in cascade.
- Each JK flip-flop operates in toggle mode by setting J = 1 and K = 1.
- The first flip-flop receives the external clock signal.
- XOR gates are used to control the clock signals of the subsequent flip-flops.
- The mode control input selects whether the counter operates in UP or DOWN counting mode.
- The counter has three output bits: QA, QB and QC.
- Since the flip-flops are triggered one after another, the circuit is called an asynchronous counter.

## Inputs
- CLK – External clock signal.
- M – Mode control input.
- J and K – Connected to logic HIGH (1) for toggle operation.

## Outputs
- QA – Least Significant Bit (LSB).
- QB – Middle bit.
- QC – Most Significant Bit (MSB).

## Mode Control Operation

| Mode (M) | Operation | Counting Sequence |
|---|---|---|
| 0 | UP Counter | 000 to 111 |
| 1 | DOWN Counter | 111 to 000 |

## Boolean Expressions

**JK Flip-Flop Toggle Condition:**

J = 1

K = 1

**Clock Equations:**

CLK_A = CLK

CLK_B = QA XOR M

CLK_C = QB XOR M

**Output Equations:**

QA(next) = NOT QA

QB(next) = NOT QB, at the active falling edge of CLK_B.

QC(next) = NOT QC, at the active falling edge of CLK_C.

## Counting Sequences

### UP Counting (M = 0)

| Clock Pulse | QC | QB | QA | Decimal |
|---|---|---|---|---|
| Initial | 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 |
| 2 | 0 | 1 | 0 | 2 |
| 3 | 0 | 1 | 1 | 3 |
| 4 | 1 | 0 | 0 | 4 |
| 5 | 1 | 0 | 1 | 5 |
| 6 | 1 | 1 | 0 | 6 |
| 7 | 1 | 1 | 1 | 7 |

Counting Sequence:

000 → 001 → 010 → 011 → 100 → 101 → 110 → 111 → 000

### DOWN Counting (M = 1)

| Clock Pulse | QC | QB | QA | Decimal |
|---|---|---|---|---|
| Initial | 1 | 1 | 1 | 7 |
| 1 | 1 | 1 | 0 | 6 |
| 2 | 1 | 0 | 1 | 5 |
| 3 | 1 | 0 | 0 | 4 |
| 4 | 0 | 1 | 1 | 3 |
| 5 | 0 | 1 | 0 | 2 |
| 6 | 0 | 0 | 1 | 1 |
| 7 | 0 | 0 | 0 | 0 |

Counting Sequence:

111 → 110 → 101 → 100 → 011 → 010 → 001 → 000 → 111

## Simulation / Observation
- When M = 0, the circuit operates as an UP counter and counts from 000 to 111.
- When M = 1, the circuit operates as a DOWN counter and counts from 111 to 000.
- The first JK flip-flop toggles for every active clock edge.
- The XOR gates control the clock transitions supplied to the second and third flip-flops.
- The output changes according to the selected counting mode.
- The counting operation repeats continuously after reaching the maximum or minimum count.
  
<img width="1910" height="1020" alt="image" src="https://github.com/user-attachments/assets/481d2e1a-98b2-4f0f-97f8-42740cd1a332" />

## Conclusion
Thus, a 3-bit asynchronous UP/DOWN counter was successfully designed and simulated using JK flip-flops and XOR gates in Logisim Evolution. The circuit performs both UP and DOWN counting operations using a single mode control input.

## Applications
- Digital clocks and timers.
- Frequency division circuits.
- Reversible digital counters.
- Digital measuring instruments.
- Industrial counting systems.
