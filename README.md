# Lua Nested Table Iteration Bug

This repository demonstrates a common, yet subtle bug in Lua related to the unordered iteration of nested tables using the `pairs` function. The bug arises from the fact that `pairs` does not guarantee any specific iteration order, leading to unexpected results when processing nested structures.

## Bug Description

The `bug.lua` file contains a function `foo` that recursively iterates through a nested table.  Due to the unordered nature of `pairs`, the order of processing nested elements is not consistent across different Lua implementations or even different runs of the same program.

## Solution

The `bugSolution.lua` provides a solution using a custom iterative function that uses a sorted table of keys to guarantee a consistent order of traversal.

## How to Reproduce

1.  Clone this repository.
2.  Run `bug.lua`.
3.  Observe the inconsistent order of output when running the script multiple times.
4. Run `bugSolution.lua` to see a consistent order.