# Neural Network Charity Analysis
## Overview of Analysis 
The purpose of this project was to use Machine Learning and Neural Networks to train on a dataset, which contains the data of 34,000 orginizations that have been funded by Alphabet Soup, and create a model that predicts the success of the orginazations with a 75% accuracy rate. They want to use this model to project the successfulness of future projects and help them determine if the charitable orginaztions that they are donating to are worth it. We preprocessed the data for the neural network, then compiled, trained and evaluated the model. And finally attempted to optimize the model to achieve the 75% accuracy rate that Alphabet Soup is requesting. 

## Results 
### Data Preprocessing
- The target variable for this nueral network model was the IS_SUCCESSFUL column. 
- The variables considered to be the features for this model were APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT. These features were encoded with the OneHotEncoder function: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', and 'INCOME_AMT'.
- The variables that were excluded from this model were: EIN and NAME.

### Compiling, Training and Evaluating the Model
- There were 2 hidden layers in my neural model, with 80 neurons in the first and 30 neurons in the second. Both of these layers used the 'relu' activation function. The output layer has one neuron and used binary 'sigmoid' activation function to classify success or not. To compile the model, I used the 'binary_crossentropy' loss function and used the 'adam' optimizer. 
- Target model performance was not reached. The accuracy score for our model was 72.96%. 
- To optimize this model, we attempted to add a hidden layer with 10 neurons using a 'relu' activation function, dropping columns with features that seemed to not add value to the dataset ('SPECIAL_CONSIDERATIONS' & 'STATUS'), and using 300 epochs instead of only 100.

## Summary 
After three attempts to optimize the model to reach the targeted 75% accuracy Alphabet Soup requested, we were unable to reach that goal. It is recommended to use a Random Forest Classifier instead of a neural network, because of the limited data points, only 34,000. Or attempt to get more data for the neural network to train on. If there is more data the neural model can prossibly increase its accuracy score and reach the target set by Alphabet Soup.
