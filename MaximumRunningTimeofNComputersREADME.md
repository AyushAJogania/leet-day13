# leet-day13

# Readme - Maximum Running Time for N Computers

This C++ solution is designed to find the maximum running time for n computers using the given batteries. It implements a binary search algorithm to efficiently search for the optimal running time that allows all n computers to run simultaneously.

## Problem Description

You are given n computers and an array `batteries` that represents the battery capacity for each computer. The `i-th` element of the `batteries` array (`batteries[i]`) denotes the capacity of the battery for the `i-th` computer. Initially, you can insert at most one battery into each computer. After that, you can remove a battery from a computer and insert it into another computer any number of times.

Your goal is to determine the maximum positive integer running speed (in minutes) that all n computers must maintain to run simultaneously using the given batteries.

## Approach

The solution follows the following approach:

1. Calculate the sum of all battery capacities and sort the `batteries` array in non-increasing order.
2. Initialize the search space by setting `low = 0` and `high = sum of all batteries`.
3. Use binary search to find the maximum running time (`mid`) that allows all n computers to run simultaneously.
4. In the binary search process, verify if it is possible to run all n computers for a given running time (`mid`) using the `check` function.
5. The `check` function calculates the total deficit (`vd`) of running time for the computers and compares it with the remaining power (`pf`) of batteries. If `pf >= vd`, then it is possible to run all n computers for the given running time `mid`.

## Functions

The code consists of the following functions:

### `check`

The `check` function verifies if it is possible to run all n computers for a given running time (`mid`). It calculates the total deficit (`vd`) of running time for the computers and compares it with the remaining power (`pf`) of batteries. If `pf >= vd`, then it is possible to run all n computers for the given running time `mid`.

### `maxRunTime`

The `maxRunTime` function finds the maximum running time using binary search. It initializes the search space by setting `low = 0` and `high = sum of all batteries`. Then, it performs a binary search to find the maximum running time that allows all n computers to run simultaneously.

## Input and Output

The input to the `maxRunTime` function is the number of computers `n` and the array `batteries` containing the battery capacity for each computer. The function returns the maximum running time required to run all n computers simultaneously.

## Time Complexity

The binary search algorithm implemented in this solution has a time complexity of O(log(sum of all batteries)). The overall time complexity of the solution is efficient and meets the given constraints.

## Constraints

- 1 <= n <= 10^5
- 1 <= batteries[i] <= 10^9

