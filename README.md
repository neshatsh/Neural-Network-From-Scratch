# Neural Network From Scratch
Manual implementation of neural network training using gradient descent and stochastic gradient descent for binary classification on the spiral dataset.
## Overview
Implements a shallow neural network from scratch to classify nested spiral patterns without using deep learning frameworks.

## Dataset
The project uses the Spiral Dataset (spiral.csv) containing:
- 200 samples with 2 features (x₁, x₂)
- Binary labels (0 or 1) representing nested spiral patterns
- Non-linearly separable data requiring neural network classification

## Neural Network Architecture
The network consists of the following layers:

1. Input Layer: 2 features (x₁, x₂)
2. Hidden Layer:
- Linear transformation: z = Wx + b (W ∈ ℝ^(1000×2), b ∈ ℝ^1000)
- ReLU activation: z' = ReLU(z)

3. Output Layer:

- Linear transformation: y = W'z' + b' (W' ∈ ℝ^(2×1000), b' ∈ ℝ²)
- Softmax activation: y' = softmax(y)

4. Loss Function: Cross-entropy loss


## Files

- gradient_descent.ipynb: Full batch gradient descent implementation
- stochastic_gradient_descent.ipynb: Mini-batch SGD implementation
- spiral.csv: Training data
- .gitignore: Python, Jupyter, macOS files

## Implementation

### Gradient Descent

- Batch size: Full dataset (200 samples)
- Learning rate: 0.1 (decay: 0.9)
- Iterations: 10,000
- Patience: 10,000

### Stochastic Gradient Descent

- Batch size: 20 samples
- Learning rate: 0.1 (decay: 0.9)
- Iterations: 10,000
- Patience: 1,000
- Data shuffling each epoch
