# Lua pairs iterator skipping elements during table modification
This repository demonstrates a subtle bug in Lua related to the `pairs` iterator and how it can skip elements when the table structure is modified during iteration.

## Bug Description
The provided Lua code uses a recursive function `foo` to traverse a nested table. Under certain conditions, `pairs` might skip elements if the table is altered during traversal. This can lead to incomplete processing of the table.

## Bug Reproduction
1. Copy the code from `bug.lua`.
2. Run the Lua code.
3. You will find the code processes incompletely because the iterator may skip elements.