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

Here, `·` represents AND and `'` represents NOT. A and B are internal signals.

## Simulation

The circuit uses four NAND gates to implement the clock-controlled SR circuit.

For the input shown in the simulation:

- S = 0
- R = 0
- CLK = 1
<img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/0453ae23-c671-4f05-a91a-cfd91c931d52" />
The circuit retains its previous state because both Set and Reset are inactive.

## Truth Table

| CLK | S | R | Q(next) | Q̅(next) | Operation |
|---|---|---|---|---|---|
| 0 | X | X | Previous state | Previous state | Hold |
| 1 | 0 | 0 | Previous state | Previous state | Hold |
| 1 | 0 | 1 | 0 | 1 | Reset |
| 1 | 1 | 0 | 1 | 0 | Set |
| 1 | 1 | 1 | Invalid | Invalid | Forbidden state |

Here, X represents either 0 or 1.

## Characteristic Table

The characteristic table shows the next state of the circuit for each combination of S, R, and the present state Q(t), when CLK = 1.

| S | R | Q(t) | Q(t+1) | Operation |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | Hold |
| 0 | 0 | 1 | 1 | Hold |
| 0 | 1 | X | 0 | Reset |
| 1 | 0 | X | 1 | Set |
| 1 | 1 | X | Invalid | Forbidden state |

## Characteristic Equation

The characteristic equation describes the relationship between the present state and the next state.

**Q(t+1) = S + R'Q(t)**

This equation is valid when the clock is HIGH and the forbidden input condition S = 1, R = 1 is excluded.

## Excitation Table

The excitation table shows the inputs required to change from the present state Q(t) to the desired next state Q(t+1).

| Q(t) | Q(t+1) | S | R |
|---|---|---|---|
| 0 | 0 | 0 | X |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 |
| 1 | 1 | X | 0 |


## Uses

- One-bit data storage.
- Set and reset control circuits.
- Registers and digital memory systems.


## Observation

The output depends on the Set, Reset, and Clock inputs. When the clock is LOW, the input NAND gates disable changes to the stored state. When the clock is HIGH, the Set and Reset inputs control the output.

## Conclusion

The clock-controlled SR circuit was designed and simulated using NAND gates in Logisim Evolution v5.0.0. The Set, Reset, and Hold operations were studied through simulation.
