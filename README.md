# Neural-Network-Charity-Analysis
With the use of Python, SKLearn, and TensorFlow, I created a neural network model to help this foundation predict whether or not to make investments to  several different applicants. 

## Overview
With my knowledge of machine learning and neural networks, I used the features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by the orginization; Alphabet Soup.

From Alphabet Soup’s business team was received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.I will be doing the following to the data;
1. Preprocess the dataset in order to compile, train, and evaluate the neural network model
2. Design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. I will think about how many inputs there are before determining the number of neurons and layers in my model. 
3. Compile, train, and evaluate your binary classification model to calculate the model’s loss and accuracy.
4. Optimize your model in order to achieve a target predictive accuracy higher than 75%. If I can't achieve an accuracy higher than 75%, you'll need to make at least three attempts to do so.

## Results
### Data PreProcessing
- What variable(s) are considered the target(s) for your model?

From the charity.csv dataset, the target for our model would be whether or not the organization chosen was successful or not. This means if the money given to the organization was used effectively or not. 

- What variable(s) are considered to be the features for your model?
In the first model, the variables I chose as features were the application type, affiliation, classification, use case of the money, organization of the company, status as active or not, the income amount of the organization, whether or not the organization was given special consideration, and finally the ask amount or funding amount requested.

- What variable(s) are neither targets nor features, and should be removed from the input data

I removed the EIN and Name of the organization as they were just identification columns and not anything that would help the machine classify whether or not they should recieve fundings. 

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Were you able to achieve the target model performance?
- What steps did you take to try and increase model performance?

## Summary
