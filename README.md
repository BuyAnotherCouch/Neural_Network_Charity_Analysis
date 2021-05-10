# Neural_Network_Charity_Analysis

## Overview

The purpose of this project is to use neural networks to help predict where the foundation should make their investments.

### Results

#### Data Preprocessing

- Target variable: IS_SUCCESSFUL
- Features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
- Neiter Targets nor Features: EIN and NAME

#### Compiling, Training, and Evaluating the Model

- For this model, 2 layers were created. Since the number of input features was 43, 80 neurons were used for the first layer as it is roughly double the features, and 30 neurons were used for the second layer. Both layers used the Rectified Linear Unit (ReLU) function to take advantage of its simplifying out. For the final layer, the Sigmoid function was used to transform the output into a range between 0 and 1. The number of epochs used was 100.

- Unfortunately this model fell short of the 75% target performance by scoring 71.29%.

- In an effort to reach the target performance, we reduced the number of features by eliminating ASK_AMT, CLASSIFICATION, USE_CASE, STATUS, ORGANIZATION, and SPECIAL_CONSIDERATIONS. We also increased the number of layers to 4 and also used 60 neurons for the first layer, 30 for the second layer, 15 for the third layer and 5 for the fourth layer. Each layer also used the Rectified Linear Unit (ReLU) function while the output layer used the Sigmoid function. The number of epochs was also increased to 2000.

### Summary

Even with our attempts to optimize the model, we still fell short of the 75% performance target with a score of %72.08. Since we are using a large dataset, it would be recommended to try the Random Forest Model as it would be able to train the data faster and may also score better on performance.
