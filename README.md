# Neural_Network_Charity_Analysis
## Overview 

The purpose of this project was to create a binary classifier, using a neural network, to attempt to predict whether applicant to a charity organization, Alphabet Soup, will be successful with their funding. The starting dataset consisted of a CSV of over 34,000 organizations that received funding from Alphabet Soup. The columns in the dataset included:

- EIN and NAME — Identification columns
- APPLICATION_TYPE — Alphabet Soup application type
- AFFILIATION — Affiliated sector of industry
- CLASSIFICATION — Government organization classification
- USE_CASE — Use case for funding
- ORGANIZATION — Organization type
- STATUS — Active status
- INCOME_AMT — Income classification
- SPECIAL_CONSIDERATIONS — Special consideration for application
- ASK_AMT — Funding amount requested
- IS_SUCCESSFUL — Was the money used effectively

## Data Preprocessing Results

### What variable(s) are considered the target(s) for your model?

-	The "IS_SUCCESSFULL" column is the target.

### What variable(s) are considered to be the features for your model?

-	The rest of the dataset's columns are the features with the exception of the "EIN" and "NAME" column which were dropped.

### What variable(s) are neither targets nor features, and should be removed from the input data?

-	I determined the "EIN", "NAME" and “STATUS” should be removed because they seemed to be independent of an applicate being successful or not.

## Compiling, Training, and Evaluating the Model Results

### How many neurons, layers, and activation functions did you select for your neural network model, and why?

- For the first iteration there were two layers used and 80 neurons were in the first layer and 30 in the second. relu and sigmoid were used as the data used was no less than 0 and we were only looking to predict if an applicant was successful.

![neurons-layers](https://github.com/backwater-graphics/Neural_Network_Charity_Analysis/blob/main/Images/neurons-layers.png)
---
 
### Were you able to achieve the target model performance?

-	No unfortunately I was not able to achieve the target model performance
-	My first run through I was able to get 66% using 8o neurons for the first layer and 20 for the second layer

![optimalization 1](https://github.com/backwater-graphics/Neural_Network_Charity_Analysis/blob/main/Images/optimalization1.png)
---
 
-	My second run through I was able to get 69% adding a hidden layer and using 87 neurons for the first layer, 12 for the second layer and 40 for the third layer

![ optimalization 2](https://github.com/backwater-graphics/Neural_Network_Charity_Analysis/blob/main/Images/optimalization2b.png)
---
 
-	For my last attempt I removed the third layer and increased the neurons to 356 for the first layer and 102 for the second layer. 
 
![ optimalization 3](https://github.com/backwater-graphics/Neural_Network_Charity_Analysis/blob/main/Images/optimalization3.png)
---

### What steps did you take to try and increase model performance?

I reprocessed the data and adjusted the bins to accommodate for the wide range of values. I also added a new layer, which did not work. In the end, increasing the number of neurons helped the most.

## Summary

The models accuracy ended up being 72.5% - we started with a data set and tried to predict whether or not the project would be successful on all of the features that we used after dropping two features that we figured to be irrelevant. Although I did not get to the accuracy of 75% that I wanted it is possible the reason for this is we may have had to drop more features which may have affected how good the neural network actually is. The best way to increase the accuracy of our model is to have solid data added to this model, the accuracy of this model will be much more concrete., or perhaps using a different model like random forest which can handle more complex data that is not linear. 
