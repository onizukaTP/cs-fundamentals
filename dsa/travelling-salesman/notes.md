# Travelling salesman

## Concept
Imagine a travelling salesman who wants to travel to 5 cities in a state. He wants to find out the efficient route to travel between cities. How can he find it? He can look at every possible order in which he could travel to the cities. That comes to **120** permutations for just **5** cities. If he wants to travel to **6** cities then the permutations will come to **720**. <br>
This is a famous problem in computer science. The brute-force solution has a time complexity of **O(n!)**. Although there are algorithms that perform better than brute force, no polynomial-time algorithm has been discovered for solving the general Travelling Salesman Problem exactly.

## Table
| Number of Cities (`n`) | Possible Routes (`n!`) |
| ---------------------: | ---------------------: |
|                      3 |                      6 |
|                      4 |                     24 |
|                      5 |                    120 |
|                      6 |                    720 |
|                      7 |                  5,040 |
|                      8 |                 40,320 |
|                      9 |                362,880 |
|                     10 |              3,628,800 |