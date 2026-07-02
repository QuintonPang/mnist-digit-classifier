# MNIST Handwritten Digit Classifier

A feedforward neural network built with PyTorch that classifies handwritten digits (0–9) from the MNIST dataset.

## Results
| Model | Train Accuracy | Test Accuracy |
|---|---|---|
| Original (no dropout) | 97.14% | 96.83% |
| With Dropout (0.2) | 94.86% | 96.36% |

Dropout reduced accuracy slightly because the original model was not overfitting to begin with (train/test gap of only 0.31%).

## Model Architecture
- Input: 28×28 grayscale images (flattened to 784)
- Hidden Layer 1: 784 → 128 (ReLU)
- Hidden Layer 2: 128 → 64 (ReLU)
- Output Layer: 64 → 10

## Training
- Optimizer: Adam (lr=0.001)
- Loss Function: CrossEntropyLoss
- Epochs: 5
- Batch Size: 64

## Key Concepts Explored
- Feedforward neural networks
- ReLU activation functions
- CrossEntropyLoss and Adam optimizer
- Dropout regularization (tested, found unnecessary due to minimal overfitting)
- Loss curve visualization
- Model save/load with `torch.save` and `torch.load`

## Files
- `mnist_digit_classifier.ipynb` — full notebook with training, evaluation, and visualizations
- `mnist_model.pth` — saved model weights

## Requirements
- Python 3
- PyTorch
- torchvision
- matplotlib
- scikit-learn
