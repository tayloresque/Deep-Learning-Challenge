** Alphabet Soup Charity: Written Report **
** Data Preprocessing


*   What variable is the target for your model?
    The 'Is_Successful' variable is the target for this model
*   What variable(s) are the features for your model? The features for this model started as the variables in all columns other than 'Is_Succesful'. We also cleaned for non-benefitial columns ('EIN' and 'Name') to not be included as features. Also, as part of my first optimization attempt I removed 'Affiliation' from features.
* What variable(s) should be removed from the input data because they are neither targets nor features? As noted above, the non-beneficial columns identified included 'EIN', 'Name', and, later, 'Affiliation'.

**Compiling, Training and Evaluating the Model


*   How many neurons, layers, and activation functions did you select for your neural network model, and why? My main/ original model included 2 hidden layers and one output layer. I started with 70 neurons in the first hidden layer as there were 69 columns, and I understand that usually the number of nuerons should be a round number close to the number of features. My original model leveraged ReLu (Rectified Linear Unit) as the activation function for the first two layers as it is good for classifications and is the most commonly used activation function used in nueral networks. Then for the output layer I chose to use the Sigmoid function as this is also good for classifications.
*   Were you able to achieve the target model performance? No, but I was very close with my first model! This model was 72.5% accurate
*   What steps did you take in your attempts to increase model performance? I leveraged most of the suggested steps to increase model performance in one of my three optimization attempts.
      *   In Optimization 1, I dropped the Affiliation column and increased the values in the classification and application types bins.
      *   In Optimization 2, I added an additional ReLu layer and added 10 additional neurons.
      *   In Optimization 3, I changed the 3 ReLu layers to Tanh functions, which are good for classifications with multiple classes. I also increased the number of epochs from 100 to 200.

**Summary: The first model performed the best, with 72.5% accuracy. The optimimizations resulted in 66.9%, 66.5% and 62% accuracy. In another optimization, I would try starting from the details I had in the original model, trying a higher binning threshold for application types, classifications, and try cleaning a few other features that might not be necessary, such as maybe status and special considerations.