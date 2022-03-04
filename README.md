# Neural_Network_Charity_Analysis
Challenge Assignment for Module 19

## Background
Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME — Identification columns
* APPLICATION_TYPE — Alphabet Soup application type
* AFFILIATION — Affiliated sector of industry
* CLASSIFICATION — Government organization classification
* USE_CASE — Use case for funding
* ORGANIZATION — Organization type
* STATUS — Active status
* INCOME_AMT — Income classification
* SPECIAL_CONSIDERATIONS — Special consideration for application
* ASK_AMT — Funding amount requested
* IS_SUCCESSFUL — Was the money used effectively


## Overview
Alphabet Soup is requesting a binary classifier that uses machine learning that can determine if applicants will be successful if funded by Alphabet Soup. We will be determining which data fields should be used by our classifier, which should be dropped, and which field is that target of the classifier. We are also determining if we can alter other characteristics of the classifier to dtermine if we can reach a 75% model accuracy.


## Results

### Data Preprocessing
* The target is the IS_SUCCESSFUL field.
* The features are every other field except the IS_SUCCESSFUL EIN, and NAME fields.  
* The variables that should be removed are the EIN and NAME fields.

### Compiling, Training, and Evaluating the Model
* 1st Attempt (Change the activation functions): 

* *  80 in Layer 1, 30 in Layer 2
* *  2 layers
* *  sigmoid and sigmoid activation function for hidden layers, and relu activation function for the output layer.

![Attempt 1 Summary]()

![Attempt 1 Results]()


* 2nd Attempt (Adding more neurons to the hidden layers): 

* *  160 in Layer 1, 60 in Layer 2
* *  2 layers
* *  relu and relu activation function for hidden layers, and sigmoid activation function for the output layer.

![Attempt 2 Summary]()

![Attempt 2 Results]()


* 3rd Attempt (Adding additional hidden layers): 

* *  80 in Layer 1, 30 in Layer 2, 60 in Layer 3
* *  3 layers
* *  relu, relu, and relu activation function for hidden layers, and sigmoid activation function for the output layer.

![Attempt 3 Summary]()

![Attempt 4 Results]()


* The samples provided by the client indicated they wanted two hidden layers with 80 and 30 neurons respectively. After that baseline was complete, I chose to use the number of neurons, layers, and activation functions above in my optimizations because I wanted to scale my neurons up and down from the baseline the client requested. 
* No. Even with the tweaks, none of the models achieved a model accuracy above about 72%.
* I tried not to change too many features in order to make sure I can make comparisons between the different attempts. The tweaks I made were to the number of neurons, adding more hidden layers, and switching up the activation functions. 


## Summary