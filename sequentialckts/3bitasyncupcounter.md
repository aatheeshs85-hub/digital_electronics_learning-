# 3-Bit Asynchronous UP Counter

## Objective

To design and simulate a 3-bit asynchronous UP counter using negative-edge-triggered JK flip-flops in Logisim Evolution v5.0.0 and verify its binary counting sequence.

## Software Used

- Logisim Evolution v5.0.0

## Description

An asynchronous UP counter is a sequential logic circuit that counts clock pulses in increasing binary order. It is also called a ripple counter because the clock transition propagates from one flip-flop to the next.

This circuit consists of three negative-edge-triggered JK flip-flops connected in cascade.

- All J and K inputs are connected to Logic 1.
- When J = 1 and K = 1, the JK flip-flop operates in toggle mode.
- The external clock is connected to the first flip-flop.
- The Q output of the first flip-flop is connected to the clock input of the second flip-flop.
- The Q output of the second flip-flop is connected to the clock input of the third flip-flop.
- Each flip-flop changes its output on the falling edge of its clock signal.
- The three outputs generate an 8-state binary counting sequence.

## Inputs and Outputs

**Inputs:**
- CLK – External clock signal.
- J and K – Connected to Logic 1.

**Outputs:**
- QA – First flip-flop output (LSB).
- QB – Second flip-flop output.
- QC – Third flip-flop output (MSB).

## Boolean Expressions

For a JK flip-flop:

Q(next) = JQ' + K'Q

Since J = 1 and K = 1:

Q(next) = Q'

Therefore, each flip-flop operates in toggle mode.

### Counter Connections

CLK1 = External CLK

CLK2 = QA

CLK3 = QB

### Toggle Conditions

QA toggles on every falling edge of the external clock.

QB toggles on every falling edge of QA.

QC toggles on every falling edge of QB.

## Truth Table

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
| 8 | 0 | 0 | 0 | 0 |

<img width="1917" height="1018" alt="Screenshot 2026-11-12 185004" src="https://github.com/user-attachments/assets/08c2a346-f0c9-46e7-83eb-b79b84067939" />


## Counting Sequence

000 → 001 → 010 → 011 → 100 → 101 → 110 → 111 → 000

## Timing Diagram

<img width="972" height="327" alt="image" src="https://github.com/user-attachments/assets/a8af17e3-33a1-4201-b527-a1f1f750b504" />


## Characteristics

- Number of flip-flops: 3
- Number of states: 8
- Modulus: 8
- Maximum count: 7
- Counting type: Binary UP counter
- Triggering method: Negative-edge triggering
- Counter type: Asynchronous (Ripple Counter)
- Flip-flop type: JK Flip-Flop

## Observation

The first JK flip-flop toggles whenever the external clock changes from HIGH to LOW.

The second flip-flop toggles whenever QA changes from HIGH to LOW. Similarly, the third flip-flop toggles whenever QB changes from HIGH to LOW.

The outputs QA, QB and QC produce an increasing binary counting sequence from 000 to 111. After reaching 111, the counter returns to 000.

Since the flip-flops operate one after another, a small propagation delay occurs between output transitions.

## Applications

- Digital clocks and timers.
- Frequency divider circuits.
- Digital event counters.
- Pulse counting systems.
- Digital measurement instruments.
- Sequential logic applications.

## Conclusion

A 3-bit negative-edge-triggered asynchronous UP counter was designed and simulated using three JK flip-flops in Logisim Evolution v5.0.0. By connecting J and K to Logic 1 and cascading the clock connections through the Q outputs, an 8-state binary counting sequence was obtained. The operation of negative-edge triggering and ripple counting was verified.
