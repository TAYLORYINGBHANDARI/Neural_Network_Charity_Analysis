# Neural_Network_Charity_Analysis
Python,pandas, Sciki-Lean,TensorFlow

## Analysis Overview

The purpose of this project is using our knowledge of TensorFlow, design a deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset.
## Resources
Data Source: charity_data.csv
Software: Python 3.7.7,Jupyter Notebook 

## Result
### Data Processing
Preprocessing Data for a Neural Network Mode

* What variable(s) are considered the target(s) for your model?
  Target variables are also known as dependent variable ,in this case we are creating a binary classification ML model. 'Is Succesfull' column can give us this binary answer.

* What variable(s) are considered to be the features for your model?
  We kept those columns as object features: 'APPLICATION_TYPE','AFFILIATION','CLASSIFICATION','USE_CASE','ORGANIZATION','INCOME_AMT','SPECIAL_CONSIDERATIONS'

* What variable(s) are neither targets nor features, and should   be removed from the input data?
    The columns EIN and NAME are identification information and have been removed from the input data.
  
### Compiling, Training, and Evaluating the Mode
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
 Initially, we had 43 features, 2 layers with 8 and 5 neurons each.We chose Relu as our hidden layer activation function and sigmoid function as output. Accuracy is 52%. 
* Were you able to achieve the target model performance?
  Yes, our accuracy jumped from 52% to 69%,the best result was 75%.
  
* What steps did you take to try and increase model performance?

  - To increase the performance of the model, We adjusted the input data, brought back the 'NAME' column data we orginially droped, bin rare occurrences in this column as 'Other'.
  - We also create bins for "ASK_AMT" column to get rid of some noisey data.
  - add more neurons to a hidden layer 
  - add 1 more hidden layer.
  - while training the model, we changed epochs several times. (epochs=100,epochs=50,epochs=200)
  - we used RELU and also Tanh as the activation function for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
## Best Result 



## Summary
Our deep learning machinese model accuracy improved from 52% to 75%.

At first sevral attempt by adding extra input values, and hidden layer and extra Epoch did help to bring the accuracy from 52% to 69%. ButIn return, we had a very high loss rate more than 1.

However, after we changed the activation function from 'RELU' to 'TANH' in the second hidden layer. The accuracy result changed dramatically to 75%, with a model lose rate of 62%.

We can say that the deep learning neural network model did reach the target of 75% accuracy. However, we still can do some adjustment or try to compare with other supervised machine learning model such as the Random Forest Classifier to generate a classified output.