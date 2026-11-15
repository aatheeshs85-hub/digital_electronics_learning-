# 3-Bit Asynchronous Down Counter

## Objective
To design and simulate a 3-bit asynchronous down counter using JK flip-flops in Logisim Evolution and observe the binary counting sequence in descending order.

## Software Used
- Logisim Evolution v5.0.0

## Description
A 3-bit asynchronous down counter is a sequential digital circuit that counts in decreasing binary order, from 7 to 0.

- It consists of three JK flip-flops connected in cascade.
- All JK flip-flops operate in toggle mode by setting J = 1 and K = 1.
- The first flip-flop receives the external clock signal.
- The output of one flip-flop controls the clock input of the next flip-flop.
- The flip-flops are triggered sequentially, producing ripple propagation.
- The counter counts down from 111 to 000 and repeats the sequence.
- Since the clock is applied only to the first flip-flop, it is called an asynchronous counter.

## Inputs
- CLK – External clock signal.
- J and K – Both inputs are connected to logic HIGH (1) to enable toggle operation.

## Outputs
- QA – Least Significant Bit (LSB).
- QB – Middle bit.
- QC – Most Significant Bit (MSB).

**Toggle condition:**

J = 1

K = 1

**Output equations:**

QA(next) = NOT QA

QB(next) = NOT QB, when the required clock transition occurs.

QC(next) = NOT QC, when the required clock transition occurs.

For a negative-edge-triggered down counter, the cascading clock connections are:

CLK_A = CLK

CLK_B = NOT QA

CLK_C = NOT QB

## Counting Sequence

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

## Simulation / Observation
- When the clock signal is applied, the first JK flip-flop toggles its output.
- The subsequent flip-flops toggle according to the output transitions of the preceding stages.
- The binary output decreases by one for every complete counting step.
- After reaching 000, the counter returns to 111 and repeats the counting cycle.
  
<img width="1917" height="1016" alt="image" src="https://github.com/user-attachments/assets/6387c0aa-ae14-48ab-ad14-2201ed5e7ac6" />

## Conclusion
Thus, a 3-bit asynchronous down counter was successfully designed and simulated using JK flip-flops in Logisim Evolution. The circuit produces the descending binary sequence from 111 to 000 and repeats continuously.

## Applications
- Digital frequency division.
- Countdown timers.
- Digital control systems.
- Event counting in reverse order.
