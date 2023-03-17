# Deutsch-Jozsa

Deutsch-Jozsa algorithm implementation and execution on a real quantum device.

### Deutsch-Jozsa problem

Given a hiden boolean function $f$ which takes as input a string of bits and returns either $0$ or $1$:

$$
f(x0, x1, x2, ...)
$$

It is guaranteed that the function to either be balanced or constant. A constant function returns all $0$'s or all $1$'s for any input, while a balanced function returns $0$'s for exactly half of all inputs and $1$'s for the other half.

The problem is to determine whether the given function is balanced or constant.

### The classical solution

In the best case, two queries can determine if the hidden boolean function, $f(x)$, is balanced: e.g. if we get both $f(0,0,0,...)→0$ and $f(1,0,0,...)→1$, then we know the function is balanced as we have obtained the two different outputs.

In the worst case, if we continue to see the same output for each input we try, we will have to check exactly half of all possible inputs plus one in order to be certain that $f(x)$ is constant. Since the total number of possible inputs is $2^n$, this implies that we need $2^{n−1}+1$ trial inputs to be certain that $f(x)$ is constant in the worst case.

### The quantum solution

This problem can be solved with 100% confidence after only one call to the function $f(x)$ using the [Deutsch-Jozsa algorithm](https://github.com/filipecorrea/deutsch-jozsa/blob/master/deutsch-jozsa.ipynb) and a quantum computer.

## Prerequisites

- [Python 3](https://www.python.org/downloads/)
- [Qiskit](https://qiskit.org)
- [IBMQ API token](https://quantum-computing.ibm.com)
