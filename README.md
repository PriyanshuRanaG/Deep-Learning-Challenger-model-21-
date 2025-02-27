# Deep Learning Model Analysis Report.
This report presents the development and evaluation of a neural network model designed to predict whether an applicant for funding will be successful in their ventures. This model has been created for the nonprofit foundation Alphabet Soup

## Data Preprocessing
The datastet was read into a pandas DataFrame and the first 5 lines were displayed to identify the target and features data to be used in the neural network. The EIN and NAME columns were identified as candidates for removal as neither target or feature. The target column was identified as the "IS_SUCCESSFUL" column with the remaining columns making up the features for the model. After dropping the non-beneficial columns the dataset was analysed to see the number of uniques values in each column. The binning techniques was used on the "APPLICATION_TYPE" and "CLASSIFICATION" columns. Firstly a value count was applied to these columns to determine a cutoff value to reduce the number of unique values all values below the cutoff's were then labelled other. The categorical data was then converted to numeric using pandas.get_dummies a

# Splitting the Data.
The data was then split into two subsets; a training set and a testing set. The default 75% to 25% train to test split was used. Finally the datasets were scaled using standard scaler ready for use be the neural network model.
# Neural Network Model Summary

## Model Architecture
Number of Input Features: The model takes in number_input_features, which is equal to the number of features in X_train.

Hidden Layers: The model has three hidden layers with the following configurations:

First hidden layer: 65 neurons, tanh activation function

Second hidden layer: 97 neurons, tanh activation function

Third hidden layer: 65 neurons, tanh activation function

Output Layer: The model has one output neuron with a sigmoid activation function, suitable for binary classification.

## Hyperparameter Tuning Using Keras Tuner
To optimize the hyperparameters such as the number of neurons, number of layers, and activation functions, Keras Tuner was used. Here is a summary of how this was achieved:

1)Define the Model-Building Function: A function that constructs and compiles the Keras model. This function uses the hp (hyperparameters) object to define the hyperparameters to be tuned.

2)Instantiate the Tuner: Use a tuner object like RandomSearch to perform the hyperparameter search.

3)Prepare the Data: Ensure the data is preprocessed and ready for training.

4)Run the Hyperparameter Search: Execute the search to find the best hyperparameters.

5)Retrieve and Train the Best Model: Get the best hyperparameters and train the final model with these settings.

## Conclusion
The model was able to achieve 0.745 accuracy, which is marginally below the intended 0.75 accuracy. With 0.5387 Loss.  

## Recomendations
Start with Logistic Regression as a baseline to understand the data and set a performance benchmark.
Experiment with Random Forests and Gradient Boosting Machines to leverage their ensemble power and ability to handle complex patterns.
Use SVMs if the data is high-dimensional and you seek robust classification boundaries.
By comparing the results from these alternative models with the deep learning model, you can identify the most effective approach for solving your classification problem. This multi-model evaluation ensures that you choose the best-performing model based on empirical evidence.
