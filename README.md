# Fashion MNIST Classification

This project focuses on an exploratory analysis of Convolutional Neural Networks (CNN) in classification of clothing items, found in a variant of the famous MNIST dataset.

## Optimal Model

### Metrics
|           |  Training |  Validation | Testing |
|-----------|-----------|-------------|---------|
| Accuracy  |   0.980   | 0.924       |  0.924  |
| Loss      |   0.0596  | 0.223       |  0.243  |


### Architecture 
* 1 Convolution Layer: 32 filters of 5x5, stride 1
* 1 Max Pooling Layer: 3x3 pool, stride 1
* 1 Convolution Layer: 32 filters of 5x5, stride 1
* 1 Max Pooling Layer: 2x2 pool, stride 2
* 1 Dense Layer: 1000 nodes, activation = ReLU
* 1 Dropout Layer: 10% (0.1)
* 1 Output Layer: 5 nodes, activation = Softmax

It contains the following hyperparameters:

* Loss: categorical crossentropy
* Optimizer: Adam
* Learning rate: step decay ($LR_i$ = 0.001, $DR$ = 0.6, $E_D$ = 9.0)
* Kernel Initializer: he_uniform
* Batch size: 64
* Epochs: 75
