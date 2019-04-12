# 60_wrapBinarySearch
[APCS] Binary search cost analysis

y = log<sub>2</sub>x means finding the exponent, that when aplied to the base two, will yield x. This exponent is equal to y.
Graph of y = log<sub>2</sub>x:

![Graph of logbase2](https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/Binary_logarithm_plot_with_ticks.svg/300px-Binary_logarithm_plot_with_ticks.svg.png)

Image courtesy of Wikipedia

Binary search: problem and solution

0. Problem: Find the index of a given element in a list that has its elements stored in ascending order with the smallest worst-case cost possible.
1. Recursive abstraction: When I am asked to find the index of an element in a list, I can find the index of that element in roughly half of the given list.
2. The recursive algorithm:
  - Decision: is the middle element of the list equal to the element being searched?
    - Solution to base case (true): return the index of the middle element.
  - Decision two: is the difference between the last and greatest element greater than zero?
    - Solution to base case (false): return a negative value;
    - Solution to recursive case: if the given element is less than the middle, call the algorithm with the bottom half of the list. Else call it with the top half.
