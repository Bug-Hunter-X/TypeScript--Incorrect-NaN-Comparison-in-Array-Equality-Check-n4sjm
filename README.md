# TypeScript: Incorrect NaN Comparison in Array Equality Check

This repository demonstrates a common error in TypeScript when comparing arrays for equality: incorrect handling of NaN (Not a Number) values.

## Bug

The `compareArrays` function in `bug.ts` attempts to compare two number arrays for equality.  However, it uses strict equality (`===`) which returns `false` when comparing `NaN` to `NaN`.

## Solution

The `bugSolution.ts` file provides a corrected version of the function. It uses `Number.isNaN` to handle NaN values appropriately, ensuring that two arrays containing NaN in the same positions are considered equal.