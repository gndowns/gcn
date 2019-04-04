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

## Dropout

Results on test set from model using different dropout rates.

| Dropout Rate | Cost      | Accuracy | Training Time |
| -----------— | --------- | -------- | ------------- |
| 0.1	         | 0.79744   | 0.80200  | 7.83903       |
| 0.2          | 0.81719   | 0.81500  | 6.70383       |
| 0.3          | 0.84194   | 0.80800  | 7.98924       |
| 0.4          | 0.87293   | 0.80200  | 5.68244       |
| 0.5          | 0.88983   | 0.80700  | 5.44867       |
| 0.6          | 0.93018   | 0.80500  | 5.44310       |
| 0.7          | 0.97307   | 0.80800  | 5.37148       |
| 0.8          | 1.08673   | 0.80100  | 5.14642       |
| 0.9          | 1.23126   | 0.82200  | 4.17396       |

## Training Epochs

Results on test set from model using different number of training epochs.

| Training Epochs | Cost     | Accuracy  | Training Time |
| --------------- | -------- | --------- | ------------- |
| 100             | 0.88983  | 0.80700   | 6.57270       |
| 200             | 0.88983  | 0.80700   | 5.64114       |
| 300             | 0.88983  | 0.80700   | 5.50688       |
| 400             | 0.88983  | 0.80700   | 5.74927       |
| 500             | 0.88983  | 0.80700   | 5.34981       |
| 600             | 0.88983  | 0.80700   | 5.36297       |
| 700             | 0.88983  | 0.80700   | 5.55295       |
| 800             | 0.88983  | 0.80700   | 5.47663       | 
| 900             | 0.88983  | 0.80700   | 5.82066       |
| 1000            | 0.88983  | 0.80700   | 5.61441       |


## Weight Decay

Results on test set from model using different weight decay values.

| Weight Decay | Cost    | Accuracy   | Training Time |
| ------------ | ------- | -----------| ------------- |
| 5e-1         | 1.95187 | 0.24900    | 10.89320      |
| 5e-2         | 1.83403 | 0.76900    | 7.81988       |
| 5e-3         | 1.19161 | 0.80500    | 9.39958       |
| 5e-4         | 0.88983 | 0.80700    | 5.62140       |
| 5e-5         | 0.81234 | 0.81200    | 2.60366       |
| 5e-6         | 0.64671 | 0.80900    | 2.63167       |
| 5e-7         | 0.61345 | 0.81000    | 2.70535       |
| 5e-8         | 0.60965 | 0.81000    | 2.97607       |
| 5e-9         | 0.60928 | 0.81000    | 2.54070       |
| 5e-10        | 0.60923 | 0.81000    | 2.60683       |


## Early stopping

Results on test set from model using different early stopping values.

| Early Stopping | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 0.70782 | 0.79800    | 19.88909      |
| 5              | 0.80570 | 0.82000    | 2.20090       |
| 10             | 0.81234 | 0.81200    | 2.56786       |
| 15             | 0.81467 | 0.80500    | 2.97880       |
| 20             | 0.81150 | 0.80600    | 3.41016       |
| 25             | 0.72610 | 0.79700    | 7.33972       |




## Max Chebyshev degree

Results on test set from model using different Max Chebyshev degrees.

| Max Chebyshev  | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 0.81234 | 0.81200    | 2.68815       |
| 1              | 0.81234 | 0.81200    | 2.84257       |
| 2              | 0.81234 | 0.81200    | 2.67853       |
| 3              | 0.81234 | 0.81200    | 2.50400       |
| 4              | 0.81234 | 0.81200    | 2.62073       |
| 5              | 0.81234 | 0.81200    | 2.51518       |