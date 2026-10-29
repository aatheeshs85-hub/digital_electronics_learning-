# Race Around Condition in JK Flip-Flop

## Objective

To study and understand the race around condition in a JK Flip-Flop using digital logic concepts.

## Description

The race around condition occurs in a level-triggered JK Flip-Flop when both inputs J and K are HIGH (J = 1, K = 1) and the clock pulse remains HIGH for a sufficiently long duration.

In this condition, the output toggles repeatedly between 0 and 1 during the same clock pulse due to feedback connections. Therefore, the final output becomes unpredictable.

<img width="320" height="507" alt="image" src="https://github.com/user-attachments/assets/47f9ebe2-7483-41c3-945f-117b8ab3bc1b" />

## Working Principle

1. When J = 0 and K = 0, the output remains unchanged.
2. When J = 0 and K = 1, the output is reset to 0.
3. When J = 1 and K = 0, the output is set to 1.
4. When J = 1 and K = 1, the output toggles.
5. If the clock pulse remains HIGH long enough, repeated toggling may occur during the same pulse. This is called the race around condition.

## Methods to Eliminate Race Around Condition

- Use a Master–Slave JK Flip-Flop.
- Use an edge-triggered JK Flip-Flop.
- Use a sufficiently short clock pulse, where appropriate.(T/2 < Propagation delay of flip flop)

## Observation

The race around condition is associated with a level-triggered JK Flip-Flop when J = K = 1 and the clock pulse duration permits repeated output toggling.


## Conclusion

The race around condition occurs when a level-triggered JK Flip-Flop repeatedly toggles its output during a single clock pulse when both J and K are HIGH. It can be eliminated using master–slave or edge-triggered JK Flip-Flops.
