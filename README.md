# Under-The-Hood
I implemented the logistic regression algorithm, which does binary classifications based on the calculations it makes based on its learning from training set, i.e. is an example of supervised learning algorithm. 

## Importing the libraries and dataset
The required libraries are imported in the first cell.<br /> 
The dataset is imported in the second cell.

## Splitting of data 
The data is once shuffled and then the data is divided into training set and validation set, with 70% of data in training set and remaining 30% in validation set. 
## Functions 
The fourth cell contains all the required functions. The description of each function is as follows:- <br />
### 1. accuracy_metric:
The first function is used to calculate the accuracy of the model on the validation set. If the predicted value for a particular row of validation set is equal to the actual value then the counter correct increments by 1, which means that when done for all the rows present in the set, it gives total number of correctly predicted values. This number is divided by the total number of values and then multiplied by 100 to give the accuracy on the set.<br />
### 2. sigmoid: 
The activation function used in logistic regression is the sigmoid function. It returns finite values that are between 0 and 1.The input for calculating the sigmoid function is given by yin = *b0+b1*x1+b2*x2+....+bn*xn. The value of this expression is calculated in this function which help of coeff list, which contains the values of bias b0,b1,b2,....,bn. The value of sigmoid function is finally returned with the use of exponential function present in numpy module. 
### 3. coeffs_gd: 
This function returns a list which consists of coefficients to be multiplied to the input values before applying sigmoid function. These values are calculated using the gradient descent algorithm, in which the coefficients/bias are being simultaneously based on the error that is calculated using the actual value and the predicted value. The aim, is of course, to minimize the error, however, it could not be made exactly zero due to finite number of epochs/iterations that could be made. 
### 4. logistic_regression:
This function returns the predictions that it make. The idea used is that if the value obtained by using sigmoid function is greater than 1/2 then the predicted value will be assigned value 1, else the output will be assigned 0. The model learns from training set and is then applied on validation set.
### 5. driver_func: 
This function acts as a driver function, that calls all other functions appropriately and returns the final outputs that are predicted by our model. 

## Call for driver function:
The driver function is called with appropriate values of learning rate and number of epochs/iterations. 
