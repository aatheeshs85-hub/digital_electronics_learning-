# Binary to BCD Converter Simulation

## Objective

To design and verify the operation of a Binary to BCD Converter using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A Binary to BCD Converter is a combinational logic circuit that converts a binary input into its corresponding decimal-coded representation using logic gates.

## Inputs and Outputs

**Inputs:** B0, B1, B2, B3

**Outputs:** A, B, C, D, E

## Boolean Expressions

- **A = (B2 · B3) + (B1 · B3)**
- **B = B2' · B3 . B1'**
- **C = (B2 · B3') + (B1 · B2)**
- **D = (B1 · B3') + (B1' · B2 · B3)**
- **E = B0**

## Simulation

The circuit uses AND, OR, and NOT gates to generate the five output bits.

For the input shown in the simulation:

- B0 = 0
- B1 = 0
- B2 = 1
- B3 = 1
<img width="1917" height="995" alt="image" src="https://github.com/user-attachments/assets/f9d4ae39-682c-478a-8afe-83d9ce5d3dc7" />

## Truth Table

| B3 | B2 | B1 | B0 | A | B | C | D | E |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 0 | 1 | 0 | 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 0 | 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 1 | 1 | 1 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 0 | 1 | 1 | 0 | 0 | 0 | 1 |
| 1 | 1 | 1 | 0 | 1 | 0 | 1 | 1 | 0 |
| 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 |

## Uses

- Digital systems for converting and processing numerical data.
- Digital display and decoding circuits.
- Combinational logic design and simulation.
- Digital electronics experiments using Logisim Evolution.

## Observation

All five output lines, A, B, C, D, and E, are included in the circuit. The output values change according to the applied binary input and the implemented logic.

## Conclusion

The five-output combinational logic circuit was designed and simulated using Logisim Evolution v5.0.0. 
