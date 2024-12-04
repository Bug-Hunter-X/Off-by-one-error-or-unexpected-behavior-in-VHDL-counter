# VHDL Counter Bug Report

This repository contains a VHDL code example demonstrating a potential bug in a simple counter implementation.  The counter is designed to count from 0 to 15 and then roll over back to 0. However, there's a subtle error in the rollover condition which might cause unexpected behavior.

## Bug Description

The bug lies in the way the counter handles the case where it reaches its maximum value (15).  There's a potential for an off-by-one error or an infinite loop. Careful examination of the `process` and the rollover condition (`if internal_count = 15 then`) is needed to identify and fix the issue. 

## How to reproduce

1. Synthesize and simulate the provided VHDL code (`bug.vhdl`).
2. Observe the counter's behavior when it reaches 15.  Does it correctly rollover to 0, or does it exhibit unexpected behavior?

## Solution

A corrected version of the code, with the bug fixed, is provided in `bugSolution.vhdl`.