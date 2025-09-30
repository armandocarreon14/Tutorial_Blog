# How to Solve Quadratic Equations in Python

## Introduction  
Quadratic equations appear in many areas such as physics, engineering, and finance. They follow the form:  

\[
![formula](https://latex.codecogs.com/svg.latex?ax^2+%2B+bx+%2B+c%3D0)
\]  

The quadratic formula gives us the solutions (roots):  

\[
![formula](https://latex.codecogs.com/svg.latex?x%20%3D%20%5Cfrac%7B-b%20%5Cpm%20%5Csqrt%7Bb%5E2-4ac%7D%7D%7B2a%7D)
\]  

In this tutorial, we’ll write a simple Python program that solves quadratic equations step by step.

---

## Step 1: Import the Math Library  
We need the `math` library for the square root function.  

```python
import math
```

## Step 2: Define the Quadric Formula
Follow the following code

```python
def quadratic_formula(a, b, c):
    # calculate the discriminant
    d = b**2 - 4*a*c
    
    # check if roots are real
    if d < 0:
        return "No real roots"
    
    # calculate the two solutions
    root1 = (-b + math.sqrt(d)) / (2*a)
    root2 = (-b - math.sqrt(d)) / (2*a)
    
    return root1, root2
```
