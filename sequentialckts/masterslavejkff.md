# Master-Slave JK Flip-Flop 

## 1. Aim
To design and simulate a Master-Slave JK Flip-Flop using NAND gates and an inverter, and verify its truth table, characteristic table, characteristic equation, and excitation table.

## 2. Introduction
A Master-Slave JK Flip-Flop is a sequential logic circuit that stores one bit of binary data. It consists of two stages: the Master and the Slave. These stages operate during opposite clock phases.

The JK Flip-Flop has two inputs, J and K, and two complementary outputs, Q and Q̅. It performs four operations: hold, set, reset, and toggle.

## 3. Components Required
- NAND gates
- NOT gate (inverter)
- J and K inputs
- Clock input
- Master outputs (Qm and Qm̅)
- Slave outputs (Q and Q̅)
  
## Circuit diagram
<img width="1536" height="821" alt="image" src="https://github.com/user-attachments/assets/3c4da5a9-cf4f-46e4-b267-85ace7135203" />


## Timing diagram
  <img width="1312" height="741" alt="image" src="https://github.com/user-attachments/assets/5399b4ba-0d67-4e72-9e34-727ea1bd072f" />


## 4. Truth Table

The truth table describes the operation of the JK Flip-Flop for different input combinations.

| J | K | Operation | Next State |
|---|---|---|---|
| 0 | 0 | Hold | Qₙ |
| 0 | 1 | Reset | 0 |
| 1 | 0 | Set | 1 |
| 1 | 1 | Toggle | Q̅ₙ |

## 5. Characteristic Table

The characteristic table shows the next state for each combination of inputs and present state.

| J | K | Present State Qₙ | Next State Qₙ₊₁ |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 |

## 6. Characteristic Equation

The characteristic equation represents the relationship between the inputs, present state, and next state.

**Qₙ₊₁ = JQ̅ₙ + K̅Qₙ**

Where:

- J and K are the input variables.
- Qₙ is the present state.
- Qₙ₊₁ is the next state.
- Q̅ₙ is the complement of the present state.
- K̅ is the complement of input K.

## 7. Excitation Table

The excitation table shows the input values required to change from the present state to the desired next state.

| Present State Qₙ | Next State Qₙ₊₁ | J | K |
|---|---|---|---|
| 0 | 0 | 0 | X |
| 0 | 1 | 1 | X |
| 1 | 0 | X | 1 |
| 1 | 1 | X | 0 |

**Note:** X represents a don't-care condition, meaning the input can be either 0 or 1.

## 8. Working Principle
1. **Hold:** When J = 0 and K = 0, the output remains unchanged.
2. **Reset:** When J = 0 and K = 1, the output becomes 0.
3. **Set:** When J = 1 and K = 0, the output becomes 1.
4. **Toggle:** When J = 1 and K = 1, the output changes to its complement.

The Master stage captures the input information during its active clock phase. The Slave stage transfers the stored information to the final output during the opposite clock phase. This arrangement prevents the race-around problem associated with a level-triggered JK Flip-Flop.

## 9. Applications
- Digital counters
- Frequency dividers
- Registers and data storage
- Sequential logic circuits
- Digital control systems

## 10. Result
The Master-Slave JK Flip-Flop was designed using NAND gates and an inverter. Its operation was studied using the truth table, characteristic table, characteristic equation, and excitation table.

## 11. Conclusion
The Master-Slave JK Flip-Flop is a one-bit storage element that performs hold, set, reset, and toggle operations. The master and slave stages operate during opposite clock phases to control the transfer of data and avoid the race-around problem.
