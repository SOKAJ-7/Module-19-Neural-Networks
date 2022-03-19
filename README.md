# Module-19-Neural-Networks

## Overview
The purpose of this analysis is to create an artificial neural network (ANN) that will use the metadata of various business to train itself to predict whether a business will be successful if funded by our client, Alphabet Soup. The deep learning model will take inputs such as: application type, affiliation, government classification, use of funding, organization type, business status, income, special considerations, and loan ask amount. Using these inputs, our model will try to determine the relationship that these variables have on the success of the loan.

## Results
# What variable(s) are considered the target(s) for your model?
The target of our ANN is the 'IS_SUCCESSFUL' column which signifies whether the money sent by Alphabet Soup was used successfully.

# What variable(s) are considered to be the features for your model?
The feature variables of our model are: application type, affiliation, government classification, use of funding, organization type, business status, income, special considerations, and loan ask amount. 

# What variable(s) are neither targets nor features, and should be removed from the input data?
The 'EIN' and 'NAME' columns relate to the identity of the applicant organization and would not benefit our ANN.

# How many neurons, layers, and activation functions did you select for your neural network model, and why?
For the first model I chose to use 2 hidden layers with 3 and 6 nodes, respectively. I started with this as I learned that it is best practice to have 2-3 nodes for every input node. For my optimization attempts I tried playing around with using much wider variety of node numbers. I added two more hidden layers and quadrupled the number of nodes in each layer. This was done in hopes that the model would be able to gain a slightly higher accuracy to reach 75% accuracy but, it only managed to increase from 0.72 to 0.73.

# Were you able to achieve the target model performance?
No, the highest accuracy score I was able to acheive was ~0.735.

# What steps did you take to try and increase model performance?
The optimization steps I took were as follows:
1. Increased neurons in each layer four-fold
2. Add two more hidden layers
3. Change activation functions. Multiple different combinations were tried. The most success was found with sigmoid and relu functions
4. Doubled the number of epochs from 100 to 200
5. Binned the 'ASK_AMT' column into 9 categories, I hoped that this would simplify the column for the ANN as before there were over 8000 unique values in the column. Again, this change had no noticeable effect

## Summary 
Most of the ANN models created in this project ended with accuracy scores around 0.72-0.735 and training losses of ~0.5 despite efforts to optimize both the dataset as well as the ANN model itself. 

If I could choose another model for this project I would attempt using a random forest machine learning model. From my research, it seems that ANNs are better suited towards high dimensional datasets with a large amount of data. This dataset isn't that complex so a random forest model may be able to at least match the ANN's performance at less computational expense.
