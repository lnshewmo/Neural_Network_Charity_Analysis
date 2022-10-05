# Neural_Network_Charity_Analysis
Optimizing neural network models to predict successful outcomes in charitable funding

---

## Overview


## Resources
- [charity_data.csv]( ) 
- Scikit Learn, Tensorflow, Keras and Pandas libraries
- Jupyter Notebook

## Results

- First Model `AlphabetSoupCharity.ipynb`
- Second Model `AlphabetSoupCharity-Optimization1.ipynb`
- Third Model `AlphabetSoupCharity-Optimization2.ipynb`
- Fourth Model `AlphabetSoupCharity-Optimization3.ipynb`

**Data Preprocessing**

 - Target - "IS_SUCCESSFUL"
 - Features - "ASK_AMT, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT"
 - Removed variables - "EIN, NAME"
 - Additional variables removed for optimizations - "STATUS, SPECIAL_CONSIDERATIONS"

**Compiling, Training and Evaluating the Model**

The initial model contained 3 neurons in each of 2 hidden layers using 'relu' activation and trained over 100 epochs.  Accuracy: 0.724

For the first optimzation everything stayed the same but 2 additional features were removed, and each hidden layer contained 5 neurons.  Accuracy: 0.725

For the next optimization, the previous optimizations remained the same but the number of epochs was increased to 200.  Accuracy: 0.727

For the final optimization, the model was able to select the best model from the following options:

- activation functions: relu or tanh
- number of neurons in the first layer
- number of hidden layers and neurons in the hidden layers

Accuracy: 0.729


The target performance of 0.750 was not achieved in any scenario.

## Summary

Using the optimizer function (`AlphabetSoupCharity-Optimization3.ipynb`) yielded the highest accuracy.  A random forest model could be tested to see if accuracy is increased.




 
