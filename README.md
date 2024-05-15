# Deep-Learning-Challenger-model-21-
## Deep Learning Model Analysis Report.
This report presents the development and evaluation of a neural network model designed to predict whether an applicant for funding will be successful in their ventures. This model has been created for the nonprofit foundation Alphabet Soup

# Data Preprocessing
The datastet was read into a pandas DataFrame and the first 5 lines were displayed to identify the target and features data to be used in the neural network. The EIN and NAME columns were identified as candidates for removal as neither target or feature. The target column was identified as the "IS_SUCCESSFUL" column with the remaining columns making up the features for the model. After dropping the non-beneficial columns the dataset was analysed to see the number of uniques values in each column. The binning techniques was used on the "APPLICATION_TYPE" and "CLASSIFICATION" columns. Firstly a value count was applied to these columns to determine a cutoff value to reduce the number of unique values all values below the cutoff's were then labelled other. The categorical data was then converted to numeric using pandas.get_dummies a

# Splitting the Data.
The data was then split into two subsets; a training set and a testing set. The default 75% to 25% train to test split was used. Finally the datasets were scaled using standard scaler ready for use be the neural network model.
