# AML Mini Project 4

## Self Loops
Results on test set from model with & without self-loops added to the graph.
This is implemented by adding the identity to the adjacneny matrix in `utils.py`.

#### Cora Dataset
| Self-Loops Included? | Cost    | Accuracy | Training Time |
| -------------------- | ------- | -------- | ------------- |
| yes (default)        | 1.00983 | 0.8130   | 10.75514      | 
| no                   | 1.07126 | 0.8090   | 10.22720      |


#### Citeseer Dataset
| Self-Loops Included? | Cost    | Accuracy | Training Time |
| -------------------- | ------- | -------- | ------------- |
| yes (default)        | 1.28585 | 0.720    | 17.72044      | 
| no                   | 1.34123 | 0.6980   | 15.64948      |


#### Pubmed Dataset
| Self-Loops Included? | Cost    | Accuracy | Training Time |
| -------------------- | ------- | -------- | ------------- |
| yes (default)        | 0.74244 | 0.7920   | 77.79246      |
| no                   | 0.77259 | 0.7810   | 73.63669      |


## Normalization
Test different normalization methods on the adjacency matrix.

#### Cora Dataset
| Normalization       | Cost    | Accuracy | Training Time |
| ------------------- | ------- | -------- | ------------- |
| Symmetric (default) | 1.00983 | 0.8130   | 10.75514      | 
| One-Sided           | 0.96358 | 0.820    | 10.72428      |
| None                | 1.00997 | 0.7860   |  1.53068\*    |


#### Citesser Dataset
| Normalization       | Cost    | Accuracy | Training Time |
| ------------------- | ------- | -------- | ------------- |
| Symmetric (default) | 1.28585 | 0.720    | 17.17417      | 
| One-sided           | 1.26499 | 0.710    | 16.26017      |  
| None                | 1.41121 | 0.6520   |  2.15959\*    |


#### Pubmed Dataset
| Normalization       | Cost    | Accuracy | Training Time |
| ------------------- | ------- | -------- | ------------- |
| Symmetric (default) | 0.74244 | 0.7920   | 77.79246      |
| One-sided           | 0.71863 | 0.780    | 62.49945\*    |
| None                | 0.94313 | 0.7590   |  8.88433\*    | 


## Optimizer

Results on test set from model using default parameters but trained on different optimizers. (Optimizers from: https://www.tensorflow.org/api_docs/python/tf/train)

### Cora

| Optimizer         | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| GradientDescent   | 1.95421       | 0.06100      | 16.54194      |
| Momentum (m=0.5)  | 1.95407       | 0.06400      | 12.64782      |
| Adagrad           | 1.95389       | 0.06900      | 12.55826      |
| RMSProp           | 1.40574       | 0.78300      | 12.82723      |
| Adam              | 1.00631       | 0.80900      | 12.71539      |

### Citeseer

| Optimizer         | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| GradientDescent   | 1.79975       | 0.15300      | 20.63144      |
| Momentum (m=0.5)  | 1.79968       | 0.15700      | 21.43084      |
| Adagrad           | 1.79961       | 0.16700      | 21.35766      |
| RMSProp           | 1.54546       | 0.71000      | 20.96380      |
| Adam              | 1.29654       | 0.71500      | 20.57743      |

### Pubmed

| Optimizer         | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| GradientDescent   | 1.10612       | 0.38200      | 175.77543     |
| Momentum (m=0.5)  | 1.10596       | 0.39200      | 176.54888     |
| Adagrad           | 1.10576       | 0.40100      | 176.33053     |
| RMSProp           | 0.76957       | 0.77100      | 177.77066     |
| Adam              | 0.72345       | 0.79200      | 152.10228     | *Early Stopping

## Activation

Results on test set from model using different activation functions.

### Cora

| Activation        | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| ReLU              | 1.00631       | 0.80900      | 12.71539      |
| Sigmoid           | 1.93431       | 0.16600      | 1.90059       | *Early Stopping
| Softmax           | 1.95022       | 0.13000      | 2.06188       | *Early Stopping

### Citeseer

| Activation        | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| ReLU              | 1.29654       | 0.71500      | 20.57743      |
| Sigmoid           | 1.81536       | 0.07700      | 1.42369       | *Early Stopping
| Softmax           | 1.79583       | 0.16900      | 1.46508       | *Early Stopping

### Pubmed

| Activation        | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| ReLU              | 0.72345       | 0.79200      | 152.10228     | *Early Stopping
| Sigmoid           | 1.09433       | 0.44800      | 24.18261      | *Early Stopping
| Softmax           | 1.10760       | 0.18000      | 11.66325      | *Early Stopping

## Learning Rate

Results on test set from model using different learning rates.
TODO: Could compare this with # epochs/number of hidden layers/number of hidden units

### Cora

| Learning Rate     | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| 0.1               | 0.96922       | 0.79600      | 3.34069       | *Early stopping
| 0.01              | 1.00631       | 0.80900      | 12.71539      |
| 0.001             | 1.82506       | 0.65800      | 12.90552      |
| 1e-4              | 1.94541       | 0.29000      | 12.90355      |
| 1e-5              | 1.95354       | 0.06900      | 13.08847      |
| 1e-6              | 1.95428       | 0.06100      | 12.88972      |

### Citeseer

| Learning Rate     | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| 0.1               | 1.30396       | 0.68600      | 4.89338       | *Early stopping
| 0.01              | 1.29654       | 0.71500      | 20.57743      |
| 0.001             | 1.73595       | 0.64900      | 21.08239      |
| 1e-4              | 1.78960       | 0.50400      | 20.60369      |
| 1e-5              | 1.79880       | 0.18700      | 20.80645      |
| 1e-6              | 1.79971       | 0.14800      | 21.09917      |

### Pubmed

| Learning Rate     | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| 0.1               | 0.72629       | 0.78600      | 30.86536      | *Early stopping
| 0.01              | 0.72345       | 0.79200      | 152.10228     | *Early Stopping
| 0.001             | 0.98747       | 0.71500      | 176.59620     |
| 1e-4              | 1.09804       | 0.56200      | 175.57387     |
| 1e-5              | 1.10568       | 0.39800      | 176.01984     |
| 1e-6              | 1.10622       | 0.36900      | 177.18335     |

## Number of hidden layers

Results on test set from model using different numbers of hidden layers.
TODO: Could compare this with # epochs/learning rate

### Cora

| Number of hidden layers  | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 0                        | 1.90896       | 0.75200      | 3.44568       | *Early Stopping
| 1                        | 1.00631       | 0.80900      | 12.71539      |
| 2                        | 0.91470       | 0.77600      | 7.12302       | *Early Stopping
| 3                        | 1.41477       | 0.45500      | 4.48670       | *Early Stopping
| 4                        | 1.16079       | 0.67000      | 6.05123       | *Early Stopping
| 5                        | 1.37210       | 0.47600      | 6.94880       | *Early Stopping

### Citeseer

| Number of hidden layers  | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 0                        | 1.78696       | 0.64700      | 0.98623       | *Early Stopping
| 1                        | 1.29654       | 0.71500      | 20.57743      |
| 2                        | 1.19124       | 0.66900      | 9.40430       | *Early Stopping
| 3                        | 1.23329       | 0.66500      | 8.33534       | *Early Stopping
| 4                        | 1.64697       | 0.38300      | 4.03902       | *Early Stopping
| 5                        | 1.71613       | 0.16900      | 4.23537       | *Early Stopping

### Pubmed

| Number of hidden layers  | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 0                        | 1.06607       | 0.72700      | 25.28811      | *Early Stopping
| 1                        | 0.72345       | 0.79200      | 152.10228     | *Early Stopping
| 2                        | 0.68209       | 0.77400      | 60.63166      | *Early Stopping
| 3                        | 0.73433       | 0.75500      | 47.27819      | *Early Stopping
| 4                        | 0.88683       | 0.74300      | 55.66350      | *Early Stopping
| 5                        | 0.89304       | 0.76100      | 44.33418      | *Early Stopping

## Number of hidden units

Results on test set from model using different numbers of hidden units.
TODO: Could compare this with # epochs/number of hidden layers/learning rate/training epochs/early stopping

### Cora

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

### Citeseer

| Number of hidden units   | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 4                        | 1.77683       | 0.35200      | 1.64180       |
| 8                        | 1.42349       | 0.69800      | 13.75726      |
| 16                       | 1.29654       | 0.71500      | 20.57743      |
| 32                       | 1.28459       | 0.71200      | 8.48483       | *Early stopping
| 64                       | 1.24263       | 0.71100      | 8.13903       | *Early stopping
| 128                      | 1.23388       | 0.70300      | 8.77516       | *Early stopping
| 256                      | 1.19609       | 0.70300      | 11.59018      | *Early stopping
| 512                      | 1.23055       | 0.68700      | 11.45539      | *Early stopping
| 1024                     | 1.26632       | 0.68600      | 12.63863      | *Early stopping

### Pubmed

| Number of hidden units   | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 4                        | 0.82043       | 0.77900      | 80.26700      |
| 8                        | 0.74628       | 0.78300      | 100.88041     | *Early Stopping
| 16                       | 0.72345       | 0.79200      | 152.10228     | *Early Stopping
| 32                       | 0.70732       | 0.79100      | 53.47373      | *Early stopping
| 64                       | 0.70803       | 0.78000      | 44.54841      | *Early stopping
| 128                      | 0.71174       | 0.79000      | 37.63908      | *Early stopping
| 256                      | 0.68859       | 0.79000      | 48.93286      | *Early stopping
| 512                      | 0.67166       | 0.79300      | 59.59024      | *Early stopping
| 1024                     | 0.71084       | 0.78000      | 63.43390      | *Early stopping

## Dropout

Results on test set from model using different dropout rates.

| Dropout Rate | Cost      | Accuracy | Training Time |
| ------------ | --------- | -------- | ------------- |
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
