# Mini Project: Plant Disease Classification

### Results:

Initial models trained for 5 epochs:

| Deep Learning Model    | F1 Score | Test Accuracy | Precision | Recall    | Loss    |
| :--------------------- | :------- | :------------ | :-------- | :-----    | :----   |
| VGG16                  | 0.81618	| 87.64500%	    | 0.85488	| 0.812005  | 0.37636 |
| VGG19                  | 0.80325	| 84.18339%	    | 0.83299	| 0.80832	| 0.50859 |
| InceptionV3            | 0.79061	| 88.10532%	    | 0.83720	| 0.79028	| 0.36811 |
| Xception               | 0.81776	| 92.67170%	    | 0.84943	| 0.82140	| 0.22193 |
| MobileNetV2            | 0.87688	| 95.47045%	    | 0.90055	| 0.87222	| 0.14963 |

Optuna Trials with different hyperparameters for MobileNetV2:

| Optuna Trial No. | Dropout | Activation | No. of Neurons in Dense Layer 1 | No. of Neurons in Dense Layer 2 | No. of Epochs            | Learning Rate               |
| :--------------- | :------ | :--------- | :------------------------------ | :------------------------------ | :------------            | :------------               |
| 0                | 0.2     | ELU        | 2048                            | 64                              | 2                        | 0.0001                      |
| 1                | 0.3     | ReLU       | 1024                            | 128                             | 2                        | 0.0001                      |
| 2                | 0.3     | ReLU       | 256                             | 64                              | 2                        | 0.0001                      |
| 3                | 0.25    | ReLU       | 2048                            | 128                             | 5                        | 0.0001                      |
| 4                | 0.25    | ELU        | 256                             | 64                              | 5                        | 0.0001                      |
| 5                | 0.25    | ReLU       | 1024                            | 512                             | 30 (Early Stopped at 22) | 0.001 (Reduced to 0.000125) |

Results of tuning MobileNetV2 with Optuna:

| Optuna Trial No.       | F1 Score | Test Accuracy | Precision | Recall    | Loss    |
| :---------------       | :------- | :------------ | :-------- | :-----    | :----   |
| 0                      | 0.85701	| 93.03995%	    | 0.89234	| 0.85215   | 0.32216 |
| 1                      | 0.83927	| 91.73265%	    | 0.87209	| 0.83465	| 0.31225 |
| 2                      | 0.78556	| 86.11674%	    | 0.80824	| 0.79580	| 0.65035 |
| 3                      | 0.86783	| 94.64187%	    | 0.89612	| 0.86338	| 0.17912 |
| 4                      | 0.85866	| 93.26091%	    | 0.88208	| 0.85656	| 0.27409 |
| 5                      | 0.90424	| 97.20125%	    | 0.91984	| 0.90075	| 0.08438 |


### Contributors:
 - Uchit Mody: 16010120030
 - Rahil Parikh: 16010120037
 - Jai Rajani: 16010120041
