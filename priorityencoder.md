# 4:2 Priority Encoder Simulation

## Objective

To design and verify the operation of a **4:2 Priority Encoder** using Logisim Evolution.

## Software Used

* Logisim Evolution v5.0.0

## Description

A **4:2 Priority Encoder** is a combinational logic circuit that converts four input lines into a 2-bit binary output. When multiple inputs are HIGH, the input with the highest priority determines the output.

In this circuit, the priority order is:

**I3 > I2 > I1 > I0**

## Inputs and Outputs

**Inputs:**

* I0, I1, I2, I3

**Outputs:**

* Y0, Y1

## Boolean Expressions

Assuming I3 has the highest priority:

**Y1 = I3 + I2**

**Y0 = I3 + (I1 · I2̅)**

## Simulation

The circuit was designed and tested using Logisim Evolution v5.0.0.

For the shown simulation:

* I1 = 1
* I2 = 1
* I3 = 0

The input I2 has higher priority than I1. Therefore, the output represents the binary code for I2.

**Output: Y1Y0 = 10**

## Truth Table

| I3 | I2 | I1 | I0 | Y1 | Y0 |
| -: | -: | -: | -: | -: | -: |
|  0 |  0 |  0 |  1 |  0 |  0 |
|  0 |  0 |  1 |  X |  0 |  1 |
|  0 |  1 |  X |  X |  1 |  0 |
|  1 |  X |  X |  X |  1 |  1 |

**X** means the input can be either 0 or 1 because a higher-priority input determines the output.

*The first row assumes a valid-input indicator is not included; a basic priority encoder generally needs an additional valid output to distinguish I0 from no active input.*

## Observation

The circuit gives priority to the highest active input. When I2 and I1 are both HIGH, I2 takes priority, producing the output code 10.
<img width="1917" height="1015" alt="image" src="https://github.com/user-attachments/assets/e5cab67a-0547-4ee0-ae72-af2e7bdcf411" />

## Conclusion

The 4:2 Priority Encoder was designed and simulated using Logisim Evolution. The simulation demonstrates how priority logic selects the highest-priority active input and generates its corresponding binary output.
