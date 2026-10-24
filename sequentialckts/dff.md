# D Flip-Flop Simulation

## Objective

To design and verify the operation of a D Flip-Flop using logic gates in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A D (Data) Flip-Flop is an edge-triggered sequential logic circuit used to store one bit of data. It has two inputs, Data (D) and Clock (CLK), and two outputs, Q and Q̅.

The output stores the value of D at the active clock edge and maintains that value until the next active clock edge.

## Inputs and Outputs

**Inputs:** D, CLK

**Outputs:** Q, Q̅

## Boolean Expressions

- **D̅ = D'**
- **A = (D · CLK)'**
- **B = (D̅ · CLK)'**
- **Q = (A · Q̅)'**
- **Q̅ = (B · Q)'**



## Simulation

The circuit uses NAND gates and a NOT gate with feedback connections.

For the input shown in the simulation:

- D = 0
- CLK = 0
- Q = 0
- Q̅ = 1

The output depends on the previously stored state and the clock-triggering condition.
<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/230bbf9b-be18-45e1-aa87-f75fd0a006b9" />

## Truth Table

| Clock Condition | D | Q (Next State) | Q̅ (Next State) | Operation |
|---|---|---|---|---|
| Active clock edge | 0 | 0 | 1 | Reset |
| Active clock edge | 1 | 1 | 0 | Set |
| No active clock edge | X | Previous state | Complement of Q | Hold |

Here, X represents either 0 or 1.

## Characteristic Table

| D | Q (Present State) | Q (Next State) |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

## Characteristic Equation

**Q (Next State) = D**

At the active clock edge, the next output state equals the input D.

## Excitation Table

| Q (Present State) | Q (Next State) | D |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

## Uses

- One-bit data storage.
- Registers in digital systems.
- Counters and shift registers.
- Synchronization of digital signals.
- Sequential logic circuit design.

## Observation

The D Flip-Flop stores the input value at the active clock edge. The output remains unchanged between active clock edges, and Q̅ provides the complement of Q during normal operation.

## Conclusion

The D Flip-Flop operation was studied using Logisim Evolution v5.0.0.
