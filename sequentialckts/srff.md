# SR Flip-Flop Simulation

## Objective

To design and verify the operation of an SR Flip-Flop using NAND gates in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

An SR (Set-Reset) Flip-Flop is a sequential logic circuit used to store one bit of data. It has three inputs: Set (S), Reset (R), and Clock (CLK), and two outputs: Q and Q̅.

The clock input controls when the Set and Reset inputs affect the output. The circuit uses NAND gates with feedback connections to maintain the stored state.

## Inputs and Outputs

**Inputs:** S, R, CLK

**Outputs:** Q, Q̅

## Boolean Expressions

- **A = (S · CLK)'**
- **B = (R · CLK)'**
- **Q = (A · Q̅)'**
- **Q̅ = (B · Q)'**


## Simulation

The circuit uses four NAND gates to implement the clock-controlled SR circuit.

For the input shown in the simulation:

- S = 0
- R = 0
- CLK = 1

The circuit retains its previous state because both Set and Reset are inactive.
<img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/0453ae23-c671-4f05-a91a-cfd91c931d52" />

## Truth Table

| CLK | S | R | Q(next) | Q̅(next) | Operation |
|---|---|---|---|---|---|
| 0 | X | X | Previous state | Previous state | Hold |
| 1 | 0 | 0 | Previous state | Previous state | Hold |
| 1 | 0 | 1 | 0 | 1 | Reset |
| 1 | 1 | 0 | 1 | 0 | Set |
| 1 | 1 | 1 | Invalid | Invalid | Forbidden state |

Here, X represents either 0 or 1.

## Uses

- One-bit data storage.
- Set and reset control circuits.
- Registers and digital memory systems.

## Observation

The output depends on the Set, Reset, and Clock inputs. When the clock is LOW, the input NAND gates disable changes to the stored state. When the clock is HIGH, the Set and Reset inputs control the output.

## Conclusion

The clock-controlled SR circuit was designed and simulated using NAND gates in Logisim Evolution v5.0.0. The Set, Reset, and Hold operations were studied through simulation.
