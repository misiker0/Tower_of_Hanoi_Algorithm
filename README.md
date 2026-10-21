# Tower of Hanoi Solver

A Python implementation of the classic **Tower of Hanoi** puzzle, solved
recursively. The function returns every move required to transfer the full
stack of disks from the first rod to the last, following the puzzle's rules.

## The Puzzle

The Tower of Hanoi is a mathematical puzzle with three rods and `n` disks of
different diameters stacked on the first rod — smallest on top, largest on
bottom. The goal is to move the entire stack to the last rod, obeying three rules:

1. Only one disk may be moved at a time.
2. Only the top-most disk of a rod can be moved.
3. A larger disk may never be placed on top of a smaller one.

## How the Algorithm Works

The solution is recursive. To move `n` disks from a source rod to a target rod:

1. Move `n - 1` disks from the source to the spare rod.
2. Move the largest disk from the source to the target rod.
3. Move the `n - 1` disks from the spare rod onto the target rod.

The recursion bottoms out at `n == 1`: move the single disk directly.

This produces the minimum possible number of moves — **2ⁿ − 1** for `n` disks.

## Usage

```python
print(hanoi_solver(3))
