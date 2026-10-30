# T Flip-Flop Simulation

## Objective

To design and verify the operation of a T (Toggle) Flip-Flop using logic gates in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A T (Toggle) Flip-Flop is an edge-triggered sequential logic circuit used to store one bit of data. It has two inputs: Toggle (T) and Clock (CLK), and two outputs: Q and Q̅.

- When T = 0, the output retains its previous state.
- When T = 1, the output toggles to the opposite state.
- The output changes only at the active clock edge.

## Inputs and Outputs

**Inputs:** T, CLK

**Outputs:** Q, Q̅

## Boolean Expressions

- **Q (Next State) = T' · Q + T · Q'**
- **Q̅ (Next State) = T' · Q' + T · Q**

Here, `·` represents AND, `+` represents OR, and `'` represents NOT.

## Simulation

The T Flip-Flop changes its output according to the Toggle input at the active clock edge.

For the input conditions:

- T = 0: Output remains unchanged.
- T = 1: Output changes to its opposite state.
<img width="1300" height="442" alt="image" src="https://github.com/user-attachments/assets/a22268c1-6b19-475c-be8f-9dfc785c8942" />

## Truth Table

| CLK | T | Q (Next State) | Q̅ (Next State) | Operation |
|---|---|---|---|---|
| Active edge | 0 | 0 | 1 | Hold |
| Active edge | 0 | 1 | 0 | Hold |
| Active edge | 1 | 0 | 1 | Toggle |
| Active edge | 1 | 1 | 0 | Toggle |
| No active edge | X | Previous state | Complement of Q | Hold |

Here, X represents either 0 or 1.

## Characteristic Table

| T | Q (Present State) | Q (Next State) |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

## Characteristic Equation

**Q (Next State) = T' · Q + T · Q'**

This equation represents the toggling operation of the T Flip-Flop.

- When T = 0, the output remains unchanged.
- When T = 1, the output changes to its complement.

## Excitation Table

| Q (Present State) | Q (Next State) | T |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

## Uses

- Binary counters.
- Frequency division circuits.
- Digital counting systems.
- Toggle control circuits.

## Observation

The T Flip-Flop maintains its previous output when T = 0 and toggles its output when T = 1 at the active clock edge. The output Q̅ is the complement of Q during normal operation.

## Conclusion

The T Flip-Flop was designed and simulated using Logisim Evolution v5.0.0. 
