## Overview of the analysis: Explain the purpose of this analysis.
* In this project, my task is to develop a binary classifier using dataset features to predict funding success for applicants, aiding Alphabet Soup, a non-profit foundation, in selecting ventures with optimal potential.

## Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model? 
* For our current dataset, the target variable is the 'IS_SUCCESSFUL' column.

What variable(s) are the features for your model? 
* The features of our model are the other columns besides 'IS_SUCCESSFUL', 'EIN' and 'NAME'. 

What variable(s) should be removed from the input data because they are neither targets nor features? 
* EIN and NAME were removed from the input data because they are neither targets nor features. 

## Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why? 
* The model has 1 hidden layer with 9 neurons and an activation function of relu (see image below). I chose binary_crossentropy as the loss function, adam as the optimiser and accuracy as the metric of our model. I chose this model out of the 3 generated models because it has the highest accuracy score. 

![Alt text](<Screenshot 2023-12-19 at 1.23.15 pm.png>)

![Alt text](<Screenshot 2023-12-19 at 1.23.32 pm.png>)

Were you able to achieve the target model performance? 
* After re-running the model 3 times using different numbers of neurons and layers, I was unable to achieve the 75% target performance. Furthermore, I tried to optimise the model by finding the best hyperparameter model using keras-tuner but I couldn't achieve the target performance after all. 

What steps did you take in your attempts to increase model performance?
* First, I tried running the model with 1 layer and 9 neurons, this model achieved an accuracy score of: 72.5%. Subsequently, I re-ran the model using 3 layers with 5 neurons for each layer, this time the accuracy score was ~72.4%. Eventually, I used keras-tuner to automate the model optimisation process by finding the best hyperparameter using different combinations of neuron and layer numbers, as well as different activation functions for the hidden layers. The final model has an accuracy score of ~72.4

## Summary: Summarise the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain any recommendation.

* In summary, our model achieved an accuracy score of 72.5% with a loss of approximately 55%. The model architecture consists of one hidden layer featuring 9 neurons and utilises the relu activation function. However, during the optimisation process using Keras-tuner, it unexpectedly generated a model with 6 layers, deviating from the suggested optimal number of 2 layers (shown in the image below). To address this, if I were to rebuild the model, I would explore alternative optimisation methods for better accuracy and reliability. One such method is grid search, a hyperparameter tuning technique provided by scikit-learn's convenient GridSearchCV class in Python. Grid search allows for an exhaustive exploration of hyperparameter combinations, aiding in the identification of the best configuration for our machine learning model.
![Alt text](<Screenshot 2023-12-18 at 11.14.09 pm.png>)
