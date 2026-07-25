# Week 1: Cost Function

## Model Parameters
For f_wb(x) = Wx + b:
- **W and b** = parameters (adjustable during training)
- **x** = feature (input, stays constant for a given example)
- **f_wb(x)** = prediction (ŷ)

A prediction is a value close to the target — rarely exact, because the best-fit line can't pass through every data point.

## Squared Error Cost Function
Measures how far predictions are from targets. Formula:

J(w,b) = (1/2m) × Σ(ŷ⁽ⁱ⁾ - y⁽ⁱ⁾)²

Steps:
1. Find difference between prediction and target
2. Square it
3. Sum across all m training examples
4. Divide by 2m (the 2 is a convention that simplifies later math)

**Goal:** Find W and b that minimize J — lower cost = more accurate model.

## Simplified Case: b = 0
When f_w(x) = Wx (one parameter), J(w) is a 2D curve. You try different values of W, compute J for each, and look for the minimum.

## Two Parameters: W and b
When both parameters are present, J(w,b) becomes a 3D surface (bowl shape). Can be visualized as a contour plot — each contour line represents points with equal cost.
