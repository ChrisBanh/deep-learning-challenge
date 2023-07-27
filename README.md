# deep-learning-challenge

## Funding Success Prediction Engine

## Overview

Alphabet Soup has funded many organisations over the years. The company wants to devise a model that can determine the success rate of an organisation that is funded by Alphabet Soup. This is through the use of machine learning and neural networks. 


## Results

* The target variable is the "IS_SUCCESSFUL" column that was converted with "pd.get_dummies". This particular column was then split intil a training and testing dataset.

* The variable that are the features of the model are the columns themselves, especially "APPLICATION_TYPE" and "CLASSIFICATIONS" that were used within this analysis. "NAME" is used for the 4th Optimisation attempt.

* The variable that we dropped for this analysis is both the "NAME" and "EIN" columns, however for the 4th Optimisation attempt, the "NAME" was included.

The initial attempt has a cutoff of 500 for the APPLICATION_TYPE and 1000 for the CLASSIFICATIONS COLUMN. Pd.get_dummies() was used to convert the dataset to numeric. It also has 2 hidden layers with 8 and 5 neurons respectively set as "relu" as the activation function. Epoch was set as 100. These are the starting points. This is results in an accuracy of 72.51%.



![alt text](https://github.com/ChrisBanh/deep-learning-challenge/blob/main/Attempt%201%20Parameter%20Changes.PNG?raw=true)

Optimisation attempt no. 1 minimised the number of cutoff values to incorporate more data into the evaluation. Increased the number of hidden layers within the model hopefully to achieve a higher target model performance. The accuracy rating for this is recorded at 72.56% for this particular run. 

![alt text](https://github.com/ChrisBanh/deep-learning-challenge/blob/main/Attempt%202%20Parameter%20Changes.PNG?raw=true)

Increased the cutoff for both the APPLICATION_TYPE and CLASSIFICAITON Columns and doubled the number of Epochs to 200 as latter epoch runs yields a higher accuracy rating. However the overall, accuracy rating is recorded at 72.38% for this run. This is lower than the initial run.

![alt text](https://github.com/ChrisBanh/deep-learning-challenge/blob/main/Attempt%203%20Parameter%20Changes.PNG?raw=true)

Reverted the cutoff values to the first optimisation attempt and adjusted the number of neurons in each layer. Change the activation function for the 3rd hidden layer to tanh. Output accuracy is recorded at 72.33%, still lower than the original run. 

![alt text](https://github.com/ChrisBanh/deep-learning-challenge/blob/main/Attempt%204%20Parameter%20Changes.PNG?raw=true)

Maintain cutoff paramters from original run, but also include the NAME feature and added a cutoff for that columns. Used the hidden layer and epoch hyperparamters from the 3rd optimisation attempt. This has a reported accuracy of 78.75% which is higher than the recommended threshold of 75%.

## Summary

In the 3 optimisations attempts that have been ran, I was unable to achieve a prediction accuracy of more than 73%. Some of the variations made from the original run worsened the prediction accuracy. No comment can be made if adjusting those parameters would noticeably change the outcome as even running the same parameters twice would yield different prediction accuracy. Only on the 4th attempt where a cutoff was applied to the number of applicants through the frequency of their applications does that yield a significantly better predictive rate of nearly 79%.  