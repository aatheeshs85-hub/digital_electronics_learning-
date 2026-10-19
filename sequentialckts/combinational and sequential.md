# Difference Between Combinational and Sequential Circuits

## Objective

To understand and compare the operation of combinational and sequential logic circuits in digital electronics.

## Software Used

- Logisim Evolution v5.0.0

## Description

Digital logic circuits are classified into two main types: **Combinational Circuits** and **Sequential Circuits**.

### 1. Combinational Circuits

A combinational circuit is a digital logic circuit in which the output depends only on the present input values. It does not store previous input information.

**Examples:**

- Half Adder
- Full Adder
- Multiplexer
- Demultiplexer
- Encoder
- Decoder
- Magnitude Comparator
- Code Converter

### 2. Sequential Circuits

A sequential circuit is a digital logic circuit in which the output depends on the present inputs and the previous state of the circuit. It uses memory elements to store information.

**Examples:**

- SR Flip-Flop
- JK Flip-Flop
- D Flip-Flop
- T Flip-Flop
- Counters
- Registers
- Shift Registers

---

## Difference Between Combinational and Sequential Circuits

| S.No. | Combinational Circuits                                 | Sequential Circuits                                      |
| ----- | ------------------------------------------------------ | -------------------------------------------------------- |
| 1     | Output depends only on present inputs.                 | Output depends on present inputs and previous state.     |
| 2     | Memory elements are not required.                      | Memory elements are required.                            |
| 3     | Feedback is generally not used.                        | Feedback is commonly used.                               |
| 4     | Clock signal is not required.                          | Clock signal is commonly used in synchronous circuits.   |
| 5     | Easier to design and implement.                        | More complex to design and implement.                    |
| 6     | Generally faster because no state storage is involved. | Timing depends on memory elements and circuit operation. |
| 7     | Examples include adders and multiplexers.              | Examples include counters and registers.                 |
| 8     | Cannot store previous input information.               | Can store previous state information.                    |

---

## Block Diagram

### Combinational Circuit

```text
Inputs ────> Combinational Logic ────> Outputs
```

The output is determined by the current input combination.

### Sequential Circuit

```text
             ┌─────────────────────┐
Inputs ─────>│  Combinational Logic│─────> Outputs
             └──────────┬──────────┘
                        ↕
                 Memory Elements
                 (Flip-Flops)
```

The memory elements store the circuit's state, allowing previous information to affect the output.

---

## Truth Table Example

### Combinational Circuit: AND Gate

| A | B | Y = A · B |
| - | - | --------- |
| 0 | 0 | 0         |
| 0 | 1 | 0         |
| 1 | 0 | 0         |
| 1 | 1 | 1         |

The output depends only on the current values of A and B.

### Sequential Circuit: D Flip-Flop

| Clock Event          | D Input | Next Output Q            |
| -------------------- | ------- | ------------------------ |
| Active clock edge    | 0       | 0                        |
| Active clock edge    | 1       | 1                        |
| No active clock edge | Changes | Holds its previous value |

A D flip-flop updates its output at the active clock edge and retains its stored state between active edges.

---

## Uses

### Combinational Circuits

1. Arithmetic operations in calculators and processors.
2. Data selection using multiplexers.
3. Binary code conversion using encoders and decoders.
4. Comparison of binary numbers.
5. Digital signal processing and control logic.

### Sequential Circuits

1. Data storage in registers.
2. Counting operations in digital counters.
3. Temporary data storage in processors.
4. Timing and control applications.
5. Memory and digital system design.

---

## Observation

- Combinational circuits generate outputs based on present input values.
- Sequential circuits use memory elements to retain their previous state.
- Combinational circuits do not require a clock for their basic operation.
- Synchronous sequential circuits use a clock to control state changes.
- Both circuit types are essential in digital electronics.

## Conclusion

The difference between combinational and sequential circuits was studied. Combinational circuits depend only on current inputs, whereas sequential circuits depend on current inputs and stored state information. Both are important for designing digital systems using Logisim Evolution.
