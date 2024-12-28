# Lua Nested Table Iteration Bug

This repository demonstrates a potential issue with relying on iteration order when using nested tables in Lua. Lua's `pairs` iterator does not guarantee a specific order of iteration, which can lead to unpredictable results when processing nested data structures.

## Bug Description
The `bug.lua` file contains a function `foo` that recursively iterates over a nested table. The order in which the nested tables are processed is not guaranteed and may change between different Lua implementations or even different runs of the same code.

## Solution
The `bugSolution.lua` file provides a solution by explicitly sorting the keys before iteration, ensuring a consistent order.  Alternatively, you could consider using a data structure which explicitly maintains order if this is important for your application (e.g., using a sequence instead of a table in some cases).