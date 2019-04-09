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
| GradientDescent   | 1.00631       | 0.80900      | 12.59550      |
| Momentum          | 1.00631       | 0.80900      | 12.92525      |
| Adagrad           | 1.00631       | 0.80900      | 16.77423      |
| RMSProp           | 1.00631       | 0.80900      | 12.66784      |
| Adam              | 1.00631       | 0.80900      | 12.71539      |

### Citeseer

| Optimizer         | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| GradientDescent   | 1.29654       | 0.71500      | 20.88426      |
| Momentum          | 1.29654       | 0.71500      | 20.75164      |
| Adagrad           | 1.29654       | 0.71500      | 21.08371      |
| RMSProp           | 1.29654       | 0.71500      | 20.65680      |
| Adam              | 1.29654       | 0.71500      | 20.57743      |

### Pubmed

| Optimizer         | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| GradientDescent   | 0.72345       | 0.79200      | 151.96015     | *Early stopping
| Momentum          | 0.72345       | 0.79200      | 152.09211     | *Early stopping
| Adagrad           | 0.72345       | 0.79200      | 152.60650     | *Early stopping
| RMSProp           | 0.72345       | 0.79200      | 153.24154     | *Early stopping
| Adam              | 0.72345       | 0.79200      | 152.10228     | *Early Stopping

## Activation

Results on test set from model using different activation functions.

### Cora

| Activation        | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| ReLU              | 1.00631       | 0.80900      | 12.71539      |
| Sigmoid           | 1.00631       | 0.80900      | 12.47668      |
| Softmax           | 1.00631       | 0.80900      | 12.55104      |

### Citeseer

| Activation        | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| ReLU              | 1.29654       | 0.71500      | 20.57743      |
| Sigmoid           | 1.29654       | 0.71500      | 20.83665      |
| Softmax           | 1.29654       | 0.71500      | 21.06329      |

### Pubmed

| Activation        | Cost          | Accuracy     | Training Time |
| ----------------- | ------------- | ------------ | ------------- |
| ReLU              | 0.72345       | 0.79200      | 152.10228     | *Early Stopping
| Sigmoid           | 0.72345       | 0.79200      | 153.10513     | *Early Stopping
| Softmax           | 0.72345       | 0.79200      | 154.14993     | *Early Stopping

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
| 0                        | 1.00631       | 0.80900      | 12.56621      |
| 1                        | 1.00631       | 0.80900      | 12.71539      |
| 2                        | 1.00631       | 0.80900      | 12.61656      |
| 3                        | 1.00631       | 0.80900      | 12.55104      |
| 4                        | 1.00631       | 0.80900      | 12.73489      |
| 5                        | 1.00631       | 0.80900      | 12.51912      |

### Citeseer

| Number of hidden layers  | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 0                        | 1.29654       | 0.71500      | 20.70505      |
| 1                        | 1.29654       | 0.71500      | 20.57743      |
| 2                        | 1.29654       | 0.71500      | 20.73452      |
| 3                        | 1.29654       | 0.71500      | 20.74501      |
| 4                        | 1.29654       | 0.71500      | 20.39031      |
| 5                        | 1.29654       | 0.71500      | 20.08235      |

### Pubmed

| Number of hidden layers  | Cost          | Accuracy     | Training Time |
| ------------------------ | ------------- | ------------ | ------------- |
| 0                        | 0.72345       | 0.79200      | 152.88821     | *Early Stopping
| 1                        | 0.72345       | 0.79200      | 152.10228     | *Early Stopping
| 2                        | 0.72345       | 0.79200      | 152.51260     | *Early Stopping
| 3                        | 0.72345       | 0.79200      | 152.38210     | *Early Stopping
| 4                        | 0.72345       | 0.79200      | 152.09245     | *Early Stopping
| 5                        | 0.72345       | 0.79200      | 152.87341     | *Early Stopping

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

### Cora

| Dropout Rate | Cost      | Accuracy | Training Time |
| ------------ | --------- | -------- | ------------- |
| 0.1	       | 0.77370   | 0.81100  | 2.48789       |
| 0.2          | 0.77380   | 0.81300  | 2.55900       |
| 0.3          | 0.77411   | 0.81300  | 2.48719       |
| 0.4          | 0.77917   | 0.81500  | 2.21157       | *early stopping @186
| 0.5          | 0.78459   | 0.81900  | 1.93356       | *early stopping @166
| 0.6          | 0.76133   | 0.81400  | 2.26451       | 
| 0.7          | 0.77312   | 0.82100  | 1.97186       | *early stopping @186
| 0.8          | 0.79277   | 0.82300  | 2.04799       |
| 0.9          | 1.06764   | 0.79800  | 1.98556       |


### Citeseer

| Dropout Rate | Cost      | Accuracy | Training Time |
| ------------ | --------- | -------- | ------------- |
| 0.1	       | 1.09848   | 0.68700  | 4.21460       |
| 0.2          | 1.10220   | 0.68700  | 4.22544       |
| 0.3          | 1.10275   | 0.69400  | 3.94120       |
| 0.4          | 1.15539   | 0.69500  | 2.84608       | *early stopping @147
| 0.5          | 1.15578   | 0.69900  | 2.68663       | *early stopping @146
| 0.6          | 1.15226   | 0.70500  | 2.64911       | *early stopping @145
| 0.7          | 1.14683   | 0.71300  | 2.58665       | *early stopping @146
| 0.8          | 1.13154   | 0.71300  | 3.12332       | *early stopping @195
| 0.9          | 1.27618   | 0.70800  | 3.05369       |

### Pubmed

| Dropout Rate | Cost      | Accuracy | Training Time |
| ------------ | --------- | -------- | ------------- |
| 0.1	       | 0.65651   | 0.76000  | 19.42807      | *early stopping @102
| 0.2          | 0.65681   | 0.76600  | 15.91506      | *early stopping @86
| 0.3          | 0.64899   | 0.77100  | 17.15949      | *early stopping @101
| 0.4          | 0.64522   | 0.76700  | 16.85851      | *early stopping @101
| 0.5          | 0.63735   | 0.76800  | 16.49610      | *early stopping @101
| 0.6          | 0.63646   | 0.77100  | 16.37050      | *early stopping @104
| 0.7          | 0.62555   | 0.77100  | 20.74273      | *early stopping @138
| 0.8          | 0.61666   | 0.76900  | 19.86997      | *early stopping @141
| 0.9          | 0.63918   | 0.76900  | 26.93809      |

## Training Epochs

Results on test set from model using different number of training epochs.

### Cora

| Training Epochs | Cost     | Accuracy  | Training Time |
| --------------- | -------- | --------- | ------------- |
| 100             | 1.25465  | 0.81300   | 1.18232       |
| 200             | 1.00631  | 0.80900   | 2.38326       |
| 300             | 0.99832  | 0.81600   | 2.44314       | *early stopping @212
| 400             | 0.99832  | 0.81600   | 2.42434       | *early stopping @212
| 500             | 0.99832  | 0.81600   | 2.40792       | *early stopping @212
| 600             | 0.99832  | 0.81600   | 2.36553       | *early stopping @212
| 700             | 0.99832  | 0.81600   | 2.46783       | *early stopping @212
| 800             | 0.99832  | 0.81600   | 2.38260       | *early stopping @212
| 900             | 0.99832  | 0.81600   | 2.38790       | *early stopping @212
| 1000            | 0.99832  | 0.81600   | 2.40301       | *early stopping @212

### Citeseer

| Training Epochs | Cost     | Accuracy  | Training Time |
| --------------- | -------- | --------- | ------------- |
| 100             | 1.47651  | 0.71200   | 1.94004       |
| 200             | 1.29654  | 0.71500   | 3.78958       |
| 300             | 1.25128  | 0.71500   | 4.59086       | *early stopping @245
| 400             | 1.25128  | 0.71500   | 4.59858       | *early stopping @245
| 500             | 1.25128  | 0.71500   | 4.45890       | *early stopping @245
| 600             | 1.25128  | 0.71500   | 4.66174       | *early stopping @245
| 700             | 1.25128  | 0.71500   | 4.56070       | *early stopping @245
| 800             | 1.25128  | 0.71500   | 4.40154       | *early stopping @245
| 900             | 1.25128  | 0.71500   | 4.58094       | *early stopping @245
| 1000            | 1.25128  | 0.71500   | 4.62257       | *early stopping @245


### Pubmed

| Training Epochs | Cost     | Accuracy  | Training Time |
| --------------- | -------- | --------- | ------------- |
| 100             | 0.77572  | 0.78400   | 16.62526      |
| 200             | 0.72345  | 0.79200   | 26.54435      | *early stopping @173
| 300             | 0.72345  | 0.79200   | 27.75325      | *early stopping @173
| 400             | 0.72345  | 0.79200   | 28.10326      | *early stopping @173
| 500             | 0.72345  | 0.79200   | 28.14500      | *early stopping @173
| 600             | 0.72345  | 0.79200   | 28.29942      | *early stopping @173
| 700             | 0.72345  | 0.79200   | 28.35029      | *early stopping @173
| 800             | 0.72345  | 0.79200   | 28.45646      | *early stopping @173
| 900             | 0.72345  | 0.79200   | 28.85993      | *early stopping @173
| 1000            | 0.72345  | 0.79200   | 28.68891      | *early stopping @173

## Weight Decay

Results on test set from model using different weight decay values.

### Cora

| Weight Decay | Cost    | Accuracy   | Training Time |
| ------------ | ------- | -----------| ------------- |
| 5e-1         | 1.94654 | 0.42500    | 1.15067       | *early stopping @ 95
| 5e-2         | 1.94772 | 0.48700    | 0.80138       | *early stopping @ 62
| 5e-3         | 1.50172 | 0.80200    | 2.26223       |
| 5e-4         | 1.00631 | 0.80900    | 2.29976       | 
| 5e-5         | 0.78459 | 0.81900    | 1.90494       | *early stopping @166
| 5e-6         | 0.66600 | 0.80500    | 1.95362       | *early stopping @164
| 5e-7         | 0.64505 | 0.80800    | 1.90494       | *early stopping @164
| 5e-8         | 0.64279 | 0.80800    | 1.86130       | *early stopping @164
| 5e-9         | 0.64255 | 0.80800    | 1.87422       | *early stopping @164
| 5e-10        | 0.64253 | 0.80800    | 1.89567       | *early stopping @164

### Citeseer 

| Weight Decay | Cost    | Accuracy   | Training Time |
| ------------ | ------- | -----------| ------------- |
| 5e-1         | 1.79278 | 0.31400    | 1.79086       | *early stopping @ 93
| 5e-2         | 1.79719 | 0.60600    | 1.04270       | *early stopping @ 50
| 5e-3         | 1.62154 | 0.69400    | 3.62586       |
| 5e-4         | 1.29654 | 0.71500    | 3.66034       | 
| 5e-5         | 1.15578 | 0.69900    | 2.73375       | *early stopping @146
| 5e-6         | 1.05434 | 0.69100    | 2.67291       | *early stopping @143
| 5e-7         | 1.03145 | 0.68400    | 2.64472       | *early stopping @143
| 5e-8         | 1.02849 | 0.68400    | 2.66707       | *early stopping @143
| 5e-9         | 1.02812 | 0.68300    | 2.64110       | *early stopping @143
| 5e-10        | 1.02812 | 0.68200    | 2.65106       | *early stopping @143


### Pubmed

| Weight Decay | Cost    | Accuracy   | Training Time |
| ------------ | ------- | -----------| ------------- |
| 5e-1         | 1.63532 | 0.31100    | 2.60775       | *early stopping @ 15
| 5e-2         | 1.15301 | 0.57000    | 2.59585       | *early stopping @ 15
| 5e-3         | 0.89171 | 0.78700    | 32.46452      |
| 5e-4         | 0.72345 | 0.79200    | 29.08713      | *early stopping @173
| 5e-5         | 0.63735 | 0.76800    | 16.81446      | *early stopping @101
| 5e-6         | 0.59885 | 0.76600    | 16.83917      | *early stopping @101
| 5e-7         | 0.59397 | 0.76600    | 17.01231      | *early stopping @101
| 5e-8         | 0.59360 | 0.76600    | 16.93164      | *early stopping @101
| 5e-9         | 0.59352 | 0.76600    | 16.96233      | *early stopping @101
| 5e-10        | 0.59351 | 0.76600    | 19.52645      | *early stopping @101


## Early stopping

Results on test set from model using different early stopping values.

### Cora

| Early Stopping | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 0.76229 | 0.81900    | 2.28043       |
| 5              | 0.78406 | 0.82200    | 1.94412       | *early stopping @164
| 10             | 0.78459 | 0.81900    | 1.91122       | *early stopping @166
| 15             | 0.78443 | 0.81800    | 1.95409       | *early stopping @170
| 20             | 0.76229 | 0.81900    | 2.30112       | 
| 25             | 0.76229 | 0.81900    | 2.24584       |

### Citeseer

| Early Stopping | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 1.11989 | 0.69800    | 3.64951       |
| 5              | 1.15540 | 0.70200    | 2.74575       | *early stopping @145
| 10             | 1.15578 | 0.69900    | 2.71404       | *early stopping @146
| 15             | 1.15573 | 0.70000    | 2.74180       | *early stopping @148
| 20             | 1.15354 | 0.69900    | 2.83581       | *early stopping @153
| 25             | 1.11989 | 0.69800    | 3.63344       |

### Pubmed

| Early Stopping | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 0.66517 | 0.77500    | 33.50235      |
| 5              | 0.63594 | 0.76700    | 16.65913      | *early stopping @99
| 10             | 0.63735 | 0.76800    | 16.97594      | *early stopping @101
| 15             | 0.63816 | 0.76900    | 17.12475      | *early stopping @102
| 20             | 0.63934 | 0.76800    | 17.36124      | *early stopping @103
| 25             | 0.64029 | 0.76800    | 17.78085      | *early stopping @106


## Max Chebyshev degree

Results on test set from model using different Max Chebyshev degrees.

### Cora

| Max Chebyshev  | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 0.78459 | 0.81900    | 1.95912       | *early stopping @166
| 1              | 0.78459 | 0.81900    | 1.93322       | *early stopping @166
| 2              | 0.78459 | 0.81900    | 1.95432       | *early stopping @166
| 3              | 0.78459 | 0.81900    | 1.93319       | *early stopping @166
| 4              | 0.78459 | 0.81900    | 1.94206       | *early stopping @166
| 5              | 0.78459 | 0.81900    | 1.96514       | *early stopping @166


### Citeseer

| Max Chebyshev  | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 1.15578 | 0.69900    | 2.78853       | *early stopping @146
| 1              | 1.15578 | 0.69900    | 2.73426       | *early stopping @146
| 2              | 1.15578 | 0.69900    | 2.79655       | *early stopping @146
| 3              | 1.15578 | 0.69900    | 2.72780       | *early stopping @146
| 4              | 1.15578 | 0.69900    | 2.79084       | *early stopping @146
| 5              | 1.15578 | 0.69900    | 2.76822       | *early stopping @146

### Pubmed

| Max Chebyshev  | Cost    | Accuracy   | Training Time |
| -------------- | ------- | ---------- | ------------- |
| 0              | 0.63735 | 0.76800    | 16.59047      | *early stopping @101
| 1              | 0.63735 | 0.76800    | 16.73723      | *early stopping @101
| 2              | 0.63735 | 0.76800    | 17.32464      | *early stopping @101
| 3              | 0.63735 | 0.76800    | 17.18759      | *early stopping @101
| 4              | 0.63735 | 0.76800    | 17.40259      | *early stopping @101
| 5              | 0.63735 | 0.76800    | 16.82687      | *early stopping @101

