# Week 1: Gradient Descent

## The Problem
We need values for w and b that minimize J(w,b). Testing every possible combination is impossible — there are infinitely many. We need an algorithm to find them automatically.

## Gradient Descent Algorithm

tmp_w = w - α × (∂J(w,b)/∂w)

tmp_b = b - α × (∂J(w,b)/∂b)

w = tmp_w

b = tmp_b

Both must be updated simultaneously in each step.

## How It Works
- Pick a starting point on the cost curve
- Compute the gradient (slope of the tangent) at that point
- The gradient tells you the direction and steepness
- Subtract the gradient × α from the current value → the parameter shifts toward the minimum
- Repeat until convergence

The sign of the gradient handles direction automatically:
- Positive gradient (right of minimum) → subtraction moves w left toward minimum
- Negative gradient (left of minimum) → subtracting a negative moves w right toward minimum

## Learning Rate (α)
- **Too large:** parameters overshoot the minimum → divergence (cost increases instead of decreasing)
- **Too small:** convergence is extremely slow — steps are tiny
- As the algorithm approaches the minimum, the gradient naturally gets smaller, so steps shrink even with a fixed α

## Key Insight
Gradient descent is not just for linear regression — it's a general optimization algorithm used across all of ML. The cost function defines *what* to minimize; gradient descent defines *how*.
