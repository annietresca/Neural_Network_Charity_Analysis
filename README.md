# Neural_Network_Charity_Analysis

![logo](https://github.com/annietresca/Neural_Network_Charity_Analysis/blob/main/Alphabet%20Soup%20logo.png)

## Overview

This analysis aims to create a binary classifier that is capable of predicting whether potential applicants will be successful if funded by Alphabet Soup, a non-profit foundation focused on environmental preservation and improving health outcomes. The project uses deep learning neural networks in the TensorFlow platform. The following methods are utilized:
1. Preprocessing the data for the neural network model
2. Compile, train and evaluate the model
3. Optimize the model


## Resources

Software: Python 3.7.9, TensorFlow 2.4.1

Data: charity_data.csv

## Results

### Data Preprocessing
- The "IS SUCCESSFUL" variable is considered the target variable for the model because we are looking to assess whether Alphabet Soup would be wise to fund the venture.
- The following variables are considered features in the model: Application type, Affiliation, Classification, Use_case, Organization, Status, Income Amt., Special Considerations and Ask Amt. These variables were then encoded and split into training and testing datasets. Standardization was then applied to these features. 
- The following variables are neither targets nor features and are thus able to be removed: "EIN" and "NAME".

### Compiling, Training and Evaluating the Model
- In the optimized model (AlphabetSoupCharity_Optimization.ipynb) four hidden layers were used. The first hidden layer used 100 neurons with a relu acitivation. The second hidden layer used 80 neurons with a relu activation. The third hidden layer used 60 neurons with a sigmoid activation. The fourth hidden layer used 40 neurons with a sigmoid activation.  
![image](https://github.com/annietresca/Neural_Network_Charity_Analysis/blob/main/Optimized-%20hidden%20layers%20and%20neurons.png) 

- While many modifications were made to the model, the best accuracy the model could produce was 72.3%.
- The following steps were taken to try and increase the model's performance:
> 1. Additional columns were removed following review: "Status" and "Special Considerations" 
> 2. Additional neurons and layers were added- a total of 4 hidden layers vs 2
> 3. Different activation functions were tried on the hidden layers to aim for better optimization- the first hidden layer was changed to relu, the second hidden layer used relu, the third hidden layer used sigmoid, the fourth hidden layer used sigmoid while the output continued using linear.


## Summary
While there were many changes made to the model, the desired target of 75% accuracy was not achieved. A recommendation for future changes to the model would be to try a Random Forest Classifier as it could combine many decision trees and generate a classified output. This could then be evaluated against the deep learning model tested in this analysis to see which performs better.
