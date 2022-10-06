# Neural Network Charity Analysis
Optimizing neural network models to predict successful outcomes in charitable funding

---

## Overview

Alphabet Soup, a non-profit foundation dedicated to bettering the enviroment, well-being and global unity is looking for a data-driven mathematical model for predicting successful versus high-risk award recipients.  The goal is to achieve a 75% accuracy in these predictions.  A neural network model was created and optimized for this purpose.

## Resources
- [charity_data.csv](https://github.com/lnshewmo/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv) 
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

The initial model contained 3 neurons in each of 2 hidden layers using 'relu' activation and trained over 100 epochs.  

![initital](https://github.com/lnshewmo/Neural_Network_Charity_Analysis/blob/main/Resources/ASC_0.png)

**Initial Model Accuracy: 0.724**

--

For the first optimzation, the activation and epochs remained the same, but 2 additional features were removed, and each hidden layer contained 5 neurons.  

![initital](https://github.com/lnshewmo/Neural_Network_Charity_Analysis/blob/main/Resources/ASC_1.png)

**First Optimization Accuracy: 0.725**

--

For the next optimization, the previous optimizations remained the same but the number of epochs was increased to 200.  

![initital](https://github.com/lnshewmo/Neural_Network_Charity_Analysis/blob/main/Resources/ASC_2.png)

**Second Optimization Accuracy: 0.727**

--

For the final optimization, the model was able to select the best model from the following options:

- activation functions: relu or tanh
- number of neurons in the first layer
- number of hidden layers and neurons in the hidden layers

![initital](https://github.com/lnshewmo/Neural_Network_Charity_Analysis/blob/main/Resources/ASC_3a.png)

![initital](https://github.com/lnshewmo/Neural_Network_Charity_Analysis/blob/main/Resources/ASC_3b.png)

**Third Optimization Accuracy: 0.729**

The target performance of 0.750 was not achieved in any scenario.

## Summary

The initial model did not meet the desired accuracy, so a stepwise optimization was performed by first removing 2 additional features from the dataset, adding additional neurons to the hidden layer and increasing the number of epochs.  In the final attempt, an optimizer function (`AlphabetSoupCharity-Optimization3.ipynb`) was implemented to allow the model to select from 2 different activation functions, and select the optimal number of layers and neurons in each layer.  This yielded the highest accuracy but still fell short of 75%.  A random forest model could be tested to see if accuracy is increased.  The random forest model can also handle nonlinear data, is robust, scalable and performs at a similar capacity as deep learning models.




 
