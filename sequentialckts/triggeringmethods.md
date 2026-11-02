# Triggering Methods in Sequential Design 

## Objective

To understand and study the different triggering methods used in sequential digital circuits.

## Description

Triggering is the process of controlling the operation of a sequential circuit using a clock signal. It determines when a latch or flip-flop responds to its input and changes its output.

There are two main types of triggering methods:

1. Level Triggering
2. Edge Triggering

## Types of Triggering Methods

### 1. Level Triggering

In level triggering, the circuit responds to the input during a particular clock level.

**A. Positive Level Triggering (Active HIGH)**

- The circuit responds when CLK = 1.
- The output can change while the clock remains HIGH.
- It is commonly used in positive-level-sensitive latches.

**B. Negative Level Triggering (Active LOW)**

- The circuit responds when CLK = 0.
- The output can change while the clock remains LOW.
- It is commonly used in negative-level-sensitive latches.

### 2. Edge Triggering

In edge triggering, the flip-flop responds only at a particular transition of the clock signal.

**A. Positive Edge Triggering (Rising Edge)**

- The output responds at the transition from 0 to 1.
- It is also called the rising edge.
- The flip-flop captures the input at this instant.

**B. Negative Edge Triggering (Falling Edge)**

- The output responds at the transition from 1 to 0.
- It is also called the falling edge.
- The flip-flop captures the input at this instant.

## Truth Table

| Triggering Method | Clock Condition | Operation |
|---|---|---|
| Positive Level | CLK = 1 | Responds during HIGH level |
| Negative Level | CLK = 0 | Responds during LOW level |
| Positive Edge | 0 → 1 | Responds at rising edge |
| Negative Edge | 1 → 0 | Responds at falling edge |

## Comparison Between Level and Edge Triggering

| Level Triggering | Edge Triggering |
|---|---|
| Responds during a particular clock level. | Responds at a clock transition. |
| Output may change throughout the active level. | Output changes only at the active edge. |
| Commonly used in latches. | Commonly used in flip-flops. |
| Can be active HIGH or LOW. | Can be rising edge or falling edge. |

## Uses

- Sequential logic circuit design.
- Registers and memory circuits.
- Digital counters.
- Microprocessors and microcontrollers.
- FPGA and VLSI circuit design.

## Observation

Level triggering allows the circuit to respond during the active clock level, whereas edge triggering allows the flip-flop to respond only at the specified clock transition.

## Conclusion

The different triggering methods used in sequential digital circuits were studied. 
