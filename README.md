<h1 align="center">Push_swap 42</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Language-C-blue" alt="C">
  <img src="https://img.shields.io/badge/Algorithm-Sorting-orange" alt="Sorting">
  <img src="https://img.shields.io/badge/42-Project-black" alt="42 Project">
  <img src="https://img.shields.io/badge/Makefile-green" alt="Makefile">
</p>

## About

Push_swap is a 42 School project focused on sorting a set of integers using two stacks and a limited number of operations.

The goal is to produce a valid sequence of operations that sorts the numbers while keeping the number of moves as low as possible.

The project focuses on:

* Sorting algorithms
* Stack data structures
* Algorithm optimization
* Complexity
* Input parsing and validation
* Memory management

## How It Works

The program starts with two stacks:

* **Stack A** contains the input numbers.
* **Stack B** is initially empty.

The program can manipulate the stacks using a limited set of operations.

The main operations are:

```text
sa   Swap the first two elements of A
sb   Swap the first two elements of B
ss   Swap A and B
pa   Push the top element of B to A
pb   Push the top element of A to B
ra   Rotate A upward
rb   Rotate B upward
rr   Rotate A and B upward
rra  Reverse rotate A
rrb  Reverse rotate B
rrr  Reverse rotate A and B
```

The objective is to finish with all numbers sorted in ascending order in Stack A.

## Project Overview

| Part           | Implementation         |
| -------------- | ---------------------- |
| Language       | C                      |
| Data Structure | Stacks                 |
| Algorithm      | Sorting / optimization |
| Build          | Makefile               |
| Input          | Command-line arguments |
| Memory         | `malloc` / `free`      |

## Installation

Clone the repository:

```bash
git clone https://github.com/elel-m-b/push_swap.git
cd push_swap
```

Compile:

```bash
make
```

## Usage

Run the program with a list of integers:

```bash
./push_swap 4 2 8 1 3
```

You can also pass the numbers as a single argument:

```bash
./push_swap "4 2 8 1 3"
```

The program outputs the operations required to sort Stack A.

Example:

```text
pb
pb
sa
pa
pa
ra
```

## Input Validation

The program handles invalid input such as:

* Non-numeric arguments
* Duplicate numbers
* Integer overflow
* Invalid integer formats
* Empty input

Example:

```bash
./push_swap 1 2 2 3
```

Output:

```text
Error
```

## Testing

You can test small sets of numbers:

```bash
./push_swap 2 1
./push_swap 3 2 1
./push_swap 5 1 4 2 3
```

For larger inputs:

```bash
./push_swap $(shuf -i 1-100 -n 100)
```

To count the number of operations:

```bash
./push_swap $(shuf -i 1-100 -n 100) | wc -l
```

You can also use the 42 Push_swap visualizer to observe the sorting process.

## Complexity

The algorithm should be designed to minimize the number of operations.

The implementation uses different strategies depending on the size and structure of the input.

The main objective is to find an efficient sequence of stack operations rather than simply sorting the numbers with a traditional sorting function.

## Cleaning

Remove object files:

```bash
make clean
```

Remove the executable and object files:

```bash
make fclean
```

Recompile everything:

```bash
make re
```


## What I Learned

This project helped me understand:

* Stack data structures
* Sorting algorithms
* Algorithmic complexity
* Optimization
* Input parsing
* Integer overflow handling
* Memory management
* Designing algorithms under constraints
* Writing efficient C code
