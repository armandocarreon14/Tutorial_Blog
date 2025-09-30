# How to Solve Quadratic Equations in Python

## Introduction  
Quadratic equations appear in many areas such as physics, engineering, and finance. They follow the form:  

![Quadratic equation formula](https://latex.codecogs.com/svg.latex?ax^2+%2B+bx+%2B+c%3D0)


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

### Example Runs

| Equation        | a | b  | c  | Output          |
|-----------------|---|----|----|-----------------|
| 2x² + 3x - 2 = 0 | 2 | 3  | -2 | (0.5, -2.0)     |
| x² - 5x + 6 = 0 | 1 | -5 | 6  | (3.0, 2.0)      |
| x² + 4x + 4 = 0 | 1 | 4  | 4  | (-2.0, -2.0)    |
| 2x² + x + 5 = 0 | 2 | 1  | 5  | No real roots   |


---

## Exercises to practice

Now it’s your turn! Try solving these equations using your `quadratic_formula` function

1. \(x^2 - 5x + 6 = 0\)  

2. \(x^2 + 4x + 4 = 0\)  

3. \(2x^2 + x + 5 = 0\)
   
Hint for the first example:

```python
print(quadratic_formula(1, -5, 6))  

---

## Conclusion

You’ve now learned how to:
- Write the quadratic formula in Python  
- Solve equations with two, one, or no real solutions  

Call to action:  
- Try plugging in your own values for `a`, `b`, and `c`.  
- Extend your code to handle complex roots using the `cmath` library.  

