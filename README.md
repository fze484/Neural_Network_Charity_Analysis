# Neural_Network_Charity_Analysis
## Overview of the analysis:
Using machine learning and neural networks, I utilized the characteristics in the given data set to develop 2 binary classifiers that can predict the likelihood of an applicant being successful if they receive funding from Alphabet Soup, a charity fund. The data set provided by Alphabet Soup's business team includes information on over 34,000 organizations that have previously received funding from the company. 

## Results:
### Data Preprocessing
* The target variable here is the column IS_SUCCESSFUL, which gauges if the money was used effectively by its recipients.
* The model's features are:
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
* The columns EIN and NAME are identification columns and removed from the dataset.

### Compiling, Training, and Evaluating the Model
* In my initial model, I picked 8 and 5 hidden nodes, in the first and second layers respectively. I used a Relu Activation function for both layers as it is the most commonly used.   
* I was close to achieving high model performance (73%)
![Test](/Resources/first_model_accuracy.png)
* According to online literature, one way to optimize a model is to neurons in the hidden layers, such as 8, and then increase the number as needed. If the network is underfitting, meaning it is not able to achieve a high accuracy on the training set, then increasing the number of neurons in the hidden layers can help to improve performance. Which is why I opted for 8 neurons in the first layer, 16 in the next and 32 in the last.  I added a third layer to increase accuray and better describe the patters in the data. I also used leaky Relu in the last layer. Either ReLU or Leaky ReLU could be used, but it is common to use ReLU as a first try and use Leaky ReLU as an alternative if needed.
![Test](/Resources/second_model_accuracy.png)

## Summary: 
As a result, altering the activation function, adding nodes and layers, and using a different activation function for the third layer didn't achieve a higher level of accuracy. However, tweaking these parameters further: using different activation functions such as tanh, different number of neurons- keeping the same amount of neurons in the hidden layers- and adding or removing a layer may help achieve the targeted accuracy.
