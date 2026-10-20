# SR Latch Using NOR and NAND Gates

## Objective

To design and simulate an SR latch using NOR gates and NAND gates in Logisim Evolution and understand how it stores one bit of data.

## Software Used

- Logisim Evolution v5.0.0

## Description

An **SR latch (Set-Reset latch)** is a basic sequential logic circuit used to store one bit of binary information. It has two inputs, Set (S) and Reset (R), and two outputs, Q and Q'.

The circuit uses two cross-coupled logic gates. The output of each gate is connected to an input of the other gate, allowing the circuit to retain its previous state.
<img width="1917" height="1011" alt="image" src="https://github.com/user-attachments/assets/0a494e38-77de-4bca-8590-ca1944716403" />

## 1. SR Latch Using NOR Gates

A NOR-based SR latch has two inputs, S and R, and two outputs, Q and Q'.

### Truth Table

| S | R | Q (Next State) | Q' (Next State) | Operation |
|---|---|---|---|---|
| 0 | 0 | Previous Q | Previous Q' | Hold |
| 0 | 1 | 0 | 1 | Reset |
| 1 | 0 | 1 | 0 | Set |
| 1 | 1 | 0 | 0 | Invalid state |

### Boolean Expressions

- Q = NOT (R + Q')
- Q' = NOT (S + Q)

### Operation

- **Hold (S=0, R=0):** The latch retains its previous state.
- **Reset (S=0, R=1):** Q becomes 0 and Q' becomes 1.
- **Set (S=1, R=0):** Q becomes 1 and Q' becomes 0.
- **Invalid (S=1, R=1):** Both outputs become 0, which violates the normal complementary-output condition.

## 2. SR Latch Using NAND Gates

A NAND-based SR latch uses two cross-coupled NAND gates. Its inputs are active-low, meaning the Set and Reset operations occur when the corresponding input is 0.

### Truth Table

| S' | R' | Q (Next State) | Q' (Next State) | Operation |
|---|---|---|---|---|
| 1 | 1 | Previous Q | Previous Q' | Hold |
| 0 | 1 | 1 | 0 | Set |
| 1 | 0 | 0 | 1 | Reset |
| 0 | 0 | 1 | 1 | Invalid state |

### Boolean Expressions

- Q = NOT (S' · Q')
- Q' = NOT (R' · Q)

### Operation

- **Hold (S'=1, R'=1):** The latch retains its previous state.
- **Set (S'=0, R'=1):** Q becomes 1 and Q' becomes 0.
- **Reset (S'=1, R'=0):** Q becomes 0 and Q' becomes 1.
- **Invalid (S'=0, R'=0):** Both outputs become 1, which violates the normal complementary-output condition.

## Applications

1. Storing one bit of binary data.
2. Switch debouncing circuits.
3. Basic memory elements in digital systems.
4. Control and sequencing circuits.
5. Building block for flip-flops and other sequential circuits.

## Observation

- The NOR latch uses active-high Set and Reset inputs.
- The NAND latch uses active-low Set and Reset inputs.
- Cross-coupled gates allow both circuits to retain their previous state.
- The invalid input combination makes both outputs equal instead of complementary.

## Conclusion

The SR latch using NOR gates and NAND gates was designed and simulated in Logisim Evolution v5.0.0. The operation of Set, Reset, Hold, and Invalid states was studied, demonstrating how an SR latch stores one bit of binary information.
