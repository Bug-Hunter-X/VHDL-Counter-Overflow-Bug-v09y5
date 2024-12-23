# VHDL Counter Overflow Bug
This repository demonstrates a common bug in VHDL code: an integer counter that overflows without proper handling.  The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

## Bug Description
The original VHDL code implements a simple counter. However, it lacks a mechanism to prevent overflow when the counter reaches its maximum value (15 in this case). This leads to undefined behavior when the counter increments past 15.

## Solution
The corrected code in `fixed_counter.vhdl` addresses the overflow issue by using a modulo operation to wrap the counter around to 0 after reaching the maximum value. This ensures predictable and correct behavior.

## How to reproduce
1. Simulate `buggy_counter.vhdl` to observe the incorrect behavior after the counter surpasses 15.
2. Simulate `fixed_counter.vhdl` to see the correct behavior with the overflow handled.
