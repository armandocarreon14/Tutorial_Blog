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
Try using the following code

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

## Step 3: Time to see if it actually works!
Use the following code to test your work

```python
print(quadratic_formula(2, 3, -2))
```

Your output should be
```python
(0.5, -2.0)
```

---

## Exercises to practice

## Exercises to Practice

Now it’s your turn! Try solving these equations using your `quadratic_formula` function

1. \(x^2 - 5x + 6 = 0\)  
   *(Hint: a = 1, b = -5, c = 6 → expect two real roots)*  

2. \(x^2 + 4x + 4 = 0\)  
   *(Hint: a = 1, b = 4, c = 4 → expect a single repeated root)*  

3. \(2x^2 + x + 5 = 0\)  
   *(Hint: a = 2, b = 1, c = 5 → expect no real roots)*  

To check, run:

```python
print(quadratic_formula(1, -5, 6))   # Example 1
print(quadratic_formula(1, 4, 4))    # Example 2
print(quadratic_formula(2, 1, 5))    # Example 3

