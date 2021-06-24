# Neural_Network_Charity_Analysis

## Overview of the analysis

Bek’s come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

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

Based on default settings:

- hidden_nodes_layer1 = 80
- hidden_nodes_layer2 = 30
- number_input_features = 43

![image](https://user-images.githubusercontent.com/76754655/123212052-2281df00-d479-11eb-8c2f-7576dc6d2bd7.png)

Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

This model achieved 54.2% accuracy with several attempts to increase the accuracy including:

- Increasing the number of hidden nodes in layer 1 (3 X number of input features)
- Increasing the number of hidden layers to include a 3rd
- Changing the activation functions: tried linear, tanh, sigmoid for a combination of hidden layers and output layer

![image](https://user-images.githubusercontent.com/76754655/123211905-f2d2d700-d478-11eb-805c-fe1bccbb7414.png)

## Summary

Overall, the results of the deep learning model show there is a 54.2% accuracy based on different variations on the number of hidden nodes in layer 1, 3 hidden layers, and different activation functions. A different model such as random forest could solve this classification problem by combining multiple smaller models into a more robust and accurate model.
