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

In the first model, I selected 2 hidden layers with 80 neurons in the first layer and 30 in the second. I chose relu as activation function for the two hidden layers. This was because I assumed the more neurons, the better the machine would be at learning and training. The reason I used relu was because most the data points were between 0-1 and the ask amount was a number the would go up to how much ever with no limit. That is why I thought relu would be the best call. I trained this model to 25 epochs which is pretty low but it seemed to hit a steady point of 73% accuracy after the 7th epoch level. 

![Screen Shot 2022-10-13 at 12 47 29 PM](https://user-images.githubusercontent.com/105755095/195668953-76e9aa52-f9bb-4c3b-b893-4ec3ad15a236.png)

- Were you able to achieve the target model performance?

The target model performance was to try and get to 75% but with the model I preformed, it never made it over 73%. 

![Screen Shot 2022-10-13 at 12 44 55 PM](https://user-images.githubusercontent.com/105755095/195668427-932821f9-5157-4a81-83ac-4739372ae7a4.png)

- What steps did you take to try and increase model performance?

In order to increase the model's performance, I tried adding more hidden layers. The first thing I did was adding a third hidden layer with 50 neurons in the first, 40 in the second, and 15 in the third. I assumed adding more layers to the model would help it train better and catch more of its mistakes. I also decreased the epochs to 15 instead of 25. 25 seemed redundent in the last model and I figured it was just taking up too much memory on my computer by running for so long. That gave me am accuracy percentage a little less than what I had before. 

The second time around, I tried making the model less busy by taking away some more features. So along witht he EIN and Name columns, I also took out Status and Special Consideration. This was because if the status of the orginazation was 0 then there was no point in considering the organization at all. With special consideration, I felt as though that column was just making the model noisy and the machine should learn without the extra columns. I also added a fourth hidden layer so that the model had an extra moment to catch its mistakes from the previous layers. I gave this layer 5 neurons. I didn't want the machine to learn slower by adding another layer. This gave an accuracy level of 73%. The best from all the tries.

The final time around, I kept the fourth hidden layer and the reduced features set, and added a slower learning rate. I believe by default the learning rate is .01. I changed it to .001 so that it slowed down and caught as much as it could to be able to give a more accurate model. However, this did not do much as the accuracy rate was the lowest at .726. 

![Screen Shot 2022-10-13 at 12 50 40 PM](https://user-images.githubusercontent.com/105755095/195671530-257a7331-ff96-43de-bc6b-7ce172416333.png)


## Summary
With all the models. there was quite a significant amount of loss. Always about .552 which is more than half the data points. The accuracy score never reached above 73% which doesn't seem to be a good model for predictions. This model gave huge losses and not a significant accuracy score. Making the model less noisy may be helpful as there are many features that the organization finds important to look at that the machine learning model finds difficult to group. Having a better understanding of the activation types may have a more significant difference on the model than I may be aware of which could also increase accuracy. 

A good model to recommend is the Random Forest model because Random Forest is good for classification problems. It is better at dealing with outliers which may be why these neural networks were having a hard time reaching a good accuracy rate. Neural Network models seems not to be the best fit, and since there is no tabular data to handle, the Random Forest Model would be able to evaluate the data with the same proficiency and most likely faster performance. 
