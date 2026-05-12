Training with CNN (CIFAR-10)
===========================

Overview
--------
This notebook trains a simple convolutional neural network on the CIFAR-10
dataset using PyTorch. It includes data transforms, a CNN with batch
normalization and dropout, a training loop with validation, and loss plots.

Notebook Contents
-----------------
- Imports and dataset transforms (resize, crop, flip, normalize)
- CIFAR-10 training and test loaders
- Visualization of a sample batch in a single horizontal row
- CNN model definition with 3 convolution blocks, batch norm, pooling, dropout
- Training loop with train/test loss tracking
- Loss curves plot
- Model checkpoint saved to "Point15.pth"

Model Architecture (Summary)
----------------------------
- Conv2d(3 -> 16) + BatchNorm2d + ReLU + MaxPool
- Conv2d(16 -> 32) + BatchNorm2d + ReLU + MaxPool
- Conv2d(32 -> 64) + BatchNorm2d + ReLU + MaxPool
- Flatten
- FC 576 -> 512 -> 256 -> 10 with Dropout between layers

How to Run
----------
1) Open Training-with-CNN.ipynb in VS Code or Jupyter.
2) Run cells top-to-bottom.
3) The dataset downloads automatically on first run.

Outputs
-------
- Training and test loss printed each epoch
- Loss curves plotted at the end
- Model weights saved to "Point15.pth"

Notes
-----
- The transform uses normalization with mean/std of (0.5, 0.5, 0.5).
- Batch size is 62 and the default epoch count is 15.
