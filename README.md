# VHDL Counter with Overflow Bug

This repository demonstrates a common bug in VHDL code: integer overflow in a counter without explicit handling.

## The Bug

The `buggy_counter.vhdl` file contains a simple counter.  However, when the counter reaches its maximum value (15), incrementing it will cause an integer overflow.  VHDL's handling of this overflow is implementation-defined, leading to unpredictable results. The code lacks robust error handling and doesn't explicitly prevent the counter from exceeding the defined range.

## The Solution

The `fixed_counter.vhdl` file provides a corrected version.  It addresses the overflow issue by checking if the counter has reached its maximum value before incrementing.  This prevents unexpected behavior and ensures the counter wraps around correctly, or a more appropriate action is taken based on the application requirement.

## How to reproduce

1. Compile and simulate `buggy_counter.vhdl` using your preferred VHDL simulator.
2. Observe the counter's behavior after it reaches 15.
3. Compile and simulate `fixed_counter.vhdl` for comparison.
