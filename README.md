# Neural_Network_Charity_Analysis

## Overview of the analysis

In support of the Alphabet Soup Charity Foundation in order to predict where to make the most favorable investments, a multiple-layered deep learning neural network is created and tested.

### Purpose

To apply machine learning and neural networks, and using the features within the provided dataset, create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup Charity Foundation.

The deliverables are:

- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model
- Deliverable 3: Optimize the Model
- Deliverable 4: Written Report

### Resources

- Data source file: charity_data.csv
- Software tools: Windows10, Jupyter Notebook, Python 3.8.3, Pandas, Scikit-learn, TensorFlow

## Results

### Data Preprocessing

What variable(s) are considered the target(s) for your model?

For this model, the target is held in the IS_SUCCESSFUL field.

What variable(s) are considered to be the features for your model?

- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE

What variable(s) are neither targets nor features, and should be removed from the input data?

- NAME
- EIN

### Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

For the initial model, the number of layers, neurons, activation functions, and epochs are shown below. The number of layers and neurons were chosen based on a stated general guideline that a basic neural network is to have two to three times the amount of neurons in the hidden layer as the number of inputs. The activation functions, the optimizer, and epochs were chosen based on guidelines from the coursework and from examples given in the challenge file. Other activation functions and epochs were used to attempt a higher accuracy for the model, and all of these are not shown in the jupyter notebook file, but these attempts did not improve the accuracy results.

- Accuracy: 72.56
- Hidden Layers: 2
- Hidden Layers Neurons: 80, 30
- Hidden Layers Activation: relu
- Output Activation: sigmoid
- Optimizer: Adam
- Epochs: 50

![image](https://user-images.githubusercontent.com/76754655/123523297-9be72080-d677-11eb-8e90-4ae07e076461.png)

Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

No, numerous attempts to increase the model's accuracy were made, none though that made any improvement. These included modifying: Hidden layers, number of neurons, pattern of neurons, activation functions for both hidden layers and for the output layer, optimizer and for number of epochs.

Noisy variables: Additional preprocessing was used to attempt to remove noisy or less significant features from the model. None of the attempts made a significant difference in the end results for Model Accuracy.

Attempt #1:

- Accuracy %: 72.38
- Hidden Layers: 2
- Hidden Layers Neurons: 90, 30
- Hidden Layers Activation: relu
- Output Activation: sigmoid
- Optimizer: Adam
- Epochs: 50

![image](https://user-images.githubusercontent.com/76754655/123523471-99d19180-d678-11eb-8054-48ba31792fbd.png)

Attempt #2:

- Accuracy %: 72.39
- Hidden Layers: 4
- Hidden Layers Neurons: 220, 120, 60, 60
- Hidden Layers Activation: relu, tanh
- Output Activation: sigmoid
- Optimizer: Adam
- Epochs: 300

![image](https://user-images.githubusercontent.com/76754655/123523493-c71e3f80-d678-11eb-9166-8b0aecde84ac.png)

Attempt #3:

- Accuracy %: 72.17
- Hidden Layers: 3
- Hidden Layers Neurons: 60, 40, 20
- Hidden Layers Activation: tanh
- Output Activation: sigmoid
- Optimizer: Adam
- Epochs: 50

![image](https://user-images.githubusercontent.com/76754655/123523542-08aeea80-d679-11eb-870d-87b485e0e9d4.png)

Attempt #4:

- Accuracy %: 72.07
- Hidden Layers: 6
- Hidden Layers Neurons: 60, 120, 240, 240, 120, 60
- Hidden Layers Activation: relu
- Output Activation: sigmoid
- Optimizer: Adam
- Epochs: 400

![image](https://user-images.githubusercontent.com/76754655/123523571-2e3bf400-d679-11eb-8133-801b227e8462.png)

Attempt #5:

- Accuracy %: 72.28
- Hidden Layers: 3
- Hidden Layers Neurons: 40, 20, 20
- Hidden Layers Activation: sigmoid, relu
- Output Activation: sigmoid
- Optimizer: Adam
- Epochs: 100

![image](https://user-images.githubusercontent.com/76754655/123523586-5a577500-d679-11eb-9964-6c05dc6393d1.png)

## Summary

In this project a deep learning neural network model was created, trained, and defined using an available data set on charitable donations to various entities. The goal was to create a model to predict the success of candidate companies receiving donations, using data of known success. Included within this project goal was to estimate the ability of the model itself with regard to the accuracy of prediction, with an accuracy score goal target of greater than 75%.

In order to attempt to improve the model accuracy, the model parameters were modified by changing available settings after training for parameters that included number of hidden layers, nodes, or neurons in each hidden layer, the activation function for each hidden layer and for the output layer, the loss function, the optimizer function, and the number of epochs. Also, the base dataset was modified to remove noisy outliers and to drop other features that would not likely be significant to the results. The overall the accuracy scores changed little from each attempt, with results from 72.1 to 72.6%.

For solution to solve a classification problem, the recommendation is to use the sigmoid activation function. With reference to the literature and documentation, the resulting sigmoid activation function values are normalized to a probability between 0 and 1, which is ideal for binary classification. The defined output of this project's model was for a binary classification, for IS_SUCCESSFUL as 1 or 0. Therefore, the sigmoid function was used for each attempt.
