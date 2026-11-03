# 4-Bit PIPO Register Simulation

## Objective

To design and verify the operation of a 4-bit Parallel-In Parallel-Out (PIPO) Register using D Flip-Flops in Logisim Evolution.

## Software Used

- Logisim Evolution v5.0.0

## Description

A Parallel-In Parallel-Out (PIPO) Register is a sequential logic circuit used to store binary data.

It consists of four D Flip-Flops connected in parallel with a common clock signal.

- Four input bits are applied simultaneously.
- Each D Flip-Flop stores one input bit.
- All flip-flops receive the same clock signal.
- Data is transferred to the outputs at the active rising edge of the clock.
- All four output bits are available simultaneously.

## Inputs and Outputs

**Inputs:** D3, D2, D1, D0, CLK

**Outputs:** Q3, Q2, Q1, Q0

## Boolean Expressions

The characteristic equation of a D Flip-Flop is:

**Q(next) = D**

For the four D Flip-Flops:

- **Q3 = D3**
- **Q2 = D2**
- **Q1 = D1**
- **Q0 = D0**

The outputs are updated simultaneously at the rising edge of the clock.

## Characteristic Table of D Flip-Flop

| D | Q (Next State) | Operation |
|---|---|---|
| 0 | 0 | Store 0 |
| 1 | 1 | Store 1 |

## Simulation

The circuit uses four D Flip-Flops connected in parallel with a common clock.

For the input combination shown in the simulation:

- D3 = 1
- D2 = 1
- D1 = 0
- D0 = 1

The corresponding outputs after the active clock edge are:

- Q3 = 1
- Q2 = 1
- Q1 = 0
- Q0 = 1
<img width="1912" height="1020" alt="image" src="https://github.com/user-attachments/assets/3524e168-2cc8-420c-8790-26e09bab7205" />

## Truth Table

| CLK | D3 | D2 | D1 | D0 | Q3 | Q2 | Q1 | Q0 |
|---|---|---|---|---|---|---|---|---|
| Rising Edge | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Rising Edge | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 |
| Rising Edge | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 |
| Rising Edge | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| Rising Edge | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 |
| Rising Edge | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 |
| Rising Edge | 0 | 1 | 1 | 0 | 0 | 1 | 1 | 0 |
| Rising Edge | 0 | 1 | 1 | 1 | 0 | 1 | 1 | 1 |
| Rising Edge | 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| Rising Edge | 1 | 0 | 0 | 1 | 1 | 0 | 0 | 1 |
| Rising Edge | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 |
| Rising Edge | 1 | 0 | 1 | 1 | 1 | 0 | 1 | 1 |
| Rising Edge | 1 | 1 | 0 | 0 | 1 | 1 | 0 | 0 |
| Rising Edge | 1 | 1 | 0 | 1 | 1 | 1 | 0 | 1 |
| Rising Edge | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 0 |
| Rising Edge | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |

**Note:** When the clock is not at its active rising edge, the outputs retain their previously stored values.

## Working Principle

1. Four binary input bits are applied simultaneously through D3, D2, D1 and D0.
2. All four D Flip-Flops receive a common clock signal.
3. At the rising edge of the clock, each flip-flop captures its corresponding input bit.
4. The stored data appears simultaneously at Q3, Q2, Q1 and Q0.
5. The outputs remain unchanged until the next active clock edge.

## Uses

- Temporary data storage.
- Microprocessor and microcontroller applications.
- Buffer storage.

## Observation

All four input bits are transferred simultaneously to their corresponding outputs at the rising edge of the clock. The outputs retain their previous values between active clock edges.

## Conclusion

A 4-bit PIPO Register was designed and simulated using four D Flip-Flops in Logisim Evolution v5.0.0.
