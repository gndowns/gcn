# AML Mini Project 4

## Optimizer

Results on test set from model using default parameters but trained on different optimizers. (Optimizers from: https://www.tensorflow.org/api_docs/python/tf/train)

| Optimizer         | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| GradientDescent   | 1.00631       | 0.80900      | 12.59550      |
| Momentum          | 1.00631       | 0.80900      | 12.92525      |
| Adagrad           | 1.00631       | 0.80900      | 16.77423      |
| RMSProp           | 1.00631       | 0.80900      | 12.66784      |
| Adam              | 1.00631       | 0.80900      | 12.71539      |

## Activation

Results on test set from model using different activation functions.

| Activation        | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| ReLU              | 1.00631       | 0.80900      | 12.71539      |
| Sigmoid           | 1.00631       | 0.80900      | 12.47668      |
| Softmax           | 1.00631       | 0.80900      | 12.55104      |

## Learning Rate

Results on test set from model using different learning rates.
TODO: Could compare this with # epochs/number of hidden layers/number of hidden units

| Learning Rate     | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| 0.1               | 0.96922       | 0.79600      | 3.34069       | *Early stopping
| 0.01              | 1.00631       | 0.80900      | 12.71539      |
| 0.001             | 1.82506       | 0.65800      | 12.90552      |
| 1e-4              | 1.94541       | 0.29000      | 12.90355      |
| 1e-5              | 1.95354       | 0.06900      | 13.08847      |
| 1e-6              | 1.95428       | 0.06100      | 12.88972      |

## Number of hidden layers

Results on test set from model using different numbers of hidden layers.
TODO: Could compare this with # epochs/learning rate

| Number of hidden layers  | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 0                        | 1.00631       | 0.80900      | 12.56621      |
| 1                        | 1.00631       | 0.80900      | 12.71539      |
| 2                        | 1.00631       | 0.80900      | 12.61656      |
| 3                        | 1.00631       | 0.80900      | 12.55104      |
| 4                        | 1.00631       | 0.80900      | 12.73489      |
| 5                        | 1.00631       | 0.80900      | 12.51912      |

## Number of hidden units

Results on test set from model using different numbers of hidden units.
TODO: Could compare this with # epochs/number of hidden layers/learning rate/training epochs/early stopping

| Number of hidden units   | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 4                        | 1.41301       | 0.74900      | 6.84848       |
| 8                        | 1.19004       | 0.80000      | 8.93986       |
| 16                       | 1.00631       | 0.80900      | 12.71539      |
| 32                       | 1.01434       | 0.81400      | 5.37668       | *Early stopping
| 64                       | 0.92625       | 0.81700      | 6.09784       | *Early stopping
| 128                      | 0.87905       | 0.81200      | 7.42148       | *Early stopping
| 256                      | 0.93944       | 0.81100      | 5.55288       | *Early stopping
| 512                      | 0.92569       | 0.80900      | 6.87969       | *Early stopping
| 1024                     | 0.88983       | 0.80700      | 10.71723      | *Early stopping