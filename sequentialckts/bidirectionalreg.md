# 4-Bit Bidirectional Shift Register Simulation

## Objective

To design and verify the operation of a 4-bit Bidirectional Shift Register using D Flip-Flops and logic gates in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A Bidirectional Shift Register is a sequential logic circuit that can shift binary data in both left and right directions.

This circuit consists of four D Flip-Flops, AND gates, OR gates, and a NOT gate. The mode control input (M) determines the direction of data shifting.

- **M = 1:** Shift Right
- **M = 0:** Shift Left

All four D Flip-Flops share a common clock signal. Data is shifted by one position during each active clock edge.

## Inputs and Outputs

**Inputs:**
- M – Mode Control
- DR – Serial Data Input for Right Shift
- DL – Serial Data Input for Left Shift
- CLK – Clock

**Outputs:**
- Q3, Q2, Q1, Q0 – Four-bit output

## Boolean Expressions

Let M be the mode control input.

For the four D Flip-Flops:

- **D3 = (M · DR) + (M' · Q2)**
- **D2 = (M · Q3) + (M' · Q1)**
- **D1 = (M · Q2) + (M' · Q0)**
- **D0 = (M · Q1) + (M' · DL)**
  
## Simulation

The circuit uses:
- Four D Flip-Flops for storing four bits.
- Eight AND gates for selecting the data inputs.
- Four OR gates for combining the selected inputs.
- One NOT gate for generating the complementary mode control signal.
- A common clock signal for synchronizing all flip-flops.

The mode control input selects the direction of shifting.

**Case 1: Shift Right (M = 1)**

- DR provides the serial input.
- Data moves from Q3 towards Q0.
- A new bit enters through the DR input.

**Case 2: Shift Left (M = 0)**

- DL provides the serial input.
- Data moves from Q0 towards Q3.
- A new bit enters through the DL input.
  
<img width="1917" height="1017" alt="image" src="https://github.com/user-attachments/assets/81990084-2be1-4401-ace2-4dbe4f895ab9" />

## Truth Table

| Mode (M) | Operation | Serial Input |
|---|---|---|
| 0 | Shift Left | DL |
| 1 | Shift Right | DR |

## Shift Operation Table

**Shift Right (M = 1)**

| Clock | Q3 | Q2 | Q1 | Q0 |
|---|---|---|---|---|
| Initial | A | B | C | D |
| After 1 clock | DR | A | B | C |
| After 2 clocks | DR2 | DR | A | B |

**Shift Left (M = 0)**

| Clock | Q3 | Q2 | Q1 | Q0 |
|---|---|---|---|---|
| Initial | A | B | C | D |
| After 1 clock | B | C | D | DL |
| After 2 clocks | C | D | DL | DL2 |

## Uses

- Serial data transmission and reception.
- Digital communication systems.
- Data storage and transfer.
- Arithmetic shift operations.
- Digital signal processing.

## Observation

The mode control input determines the direction of data shifting. When M = 1, data shifts towards Q0, and when M = 0, data shifts towards Q3. The serial inputs DR and DL provide new data bits during the respective shifting operations.

## Conclusion

A 4-bit Bidirectional Shift Register was successfully designed and simulated using D Flip-Flops and logic gates in Logisim Evolution v5.0.0.
