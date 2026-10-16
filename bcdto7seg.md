# BCD to 7-Segment Display Decoder Simulation

## Objective

To design and verify the operation of a **BCD to 7-Segment Display Decoder** using Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A **BCD to 7-Segment Display Decoder** is a combinational logic circuit that converts a 4-bit Binary Coded Decimal (BCD) input into seven output signals to display decimal digits from 0 to 9.

The four inputs are represented by **A, B, C, D**, and the seven outputs are represented by **a, b, c, d, e, f, g**.

Each output controls one segment of the display. Depending on the input combination, the required segments glow to represent the corresponding decimal digit.

## Inputs and Outputs

**Input Lines:**
- A – Most Significant Bit (MSB)
- B
- C
- D – Least Significant Bit (LSB)

**Output Lines:**
- a, b, c, d, e, f, g

## Boolean Expressions

The simplified Boolean expressions for the seven segment outputs are:

- **a = A + C + BD + B'D'**
- **b = B' + C'D' + CD**
- **c = B + D + C'**
- **d = A + B'C + B'D' + CD' + BC'D**
- **e = B'D' + CD'**
- **f = A + C'D' + BC' + BD'**
- **g = A + B'C + BC' + CD'**


## Truth Table

| Decimal Digit | A | B | C | D | a | b | c | d | e | f | g |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | 0 | 0 | 0 |
| 2 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | 1 | 1 | 0 | 1 |
| 3 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 0 | 1 |
| 4 | 0 | 1 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| 5 | 0 | 1 | 0 | 1 | 1 | 0 | 1 | 1 | 0 | 1 | 1 |
| 6 | 0 | 1 | 1 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | 1 |
| 7 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 |
| 8 | 1 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| 9 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 |

**Output convention:** 1 means the segment is ON, and 0 means the segment is OFF. The table assumes a common-cathode-style active-high display.

## Simulation

The circuit was designed using AND, OR, and NOT gates in Logisim Evolution.

The four input switches generate BCD combinations. The logic gates process these inputs and produce seven output signals.

The outputs control the corresponding segments of the display to represent decimal digits from 0 to 9.

<img width="1917" height="1012" alt="image" src="https://github.com/user-attachments/assets/0ac0e96a-d062-4b5d-9539-595d40635bd4" />

## Uses of BCD to 7-Segment Decoder

1. **Digital clocks:** Displays hours, minutes, and seconds.
2. **Calculators:** Displays numerical results.
3. **Digital counters:** Displays the count in decimal form.
4. **Measuring instruments:** Displays voltage, current, temperature, and other measured values.
5. **Electronic meters:** Used in digital energy meters and counting systems.
6. **Elevator displays:** Displays floor numbers.
7. **Digital weighing machines:** Displays measured weight.
8. **Industrial control panels:** Displays numerical readings and process values.

## Observation

- The four input bits were applied to the decoder circuit.
- The AND, OR, and NOT gates generated the required segment signals.
- The seven outputs represented the individual display segments.
- The output combinations were checked for valid BCD inputs from 0000 to 1001.
- The display represented the corresponding decimal digits when the segment connections and logic were correct.

## Conclusion

The BCD to 7-Segment Display Decoder was designed and simulated using Logisim Evolution v5.0.0.
