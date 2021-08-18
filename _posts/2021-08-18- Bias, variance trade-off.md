 

### Bias

\-   Error between average model prediction and ground truth

\-   Tell us the capacity of the underlying model to predict the values

### Variance

\-   Average variability in the model prediction for the given dataset

\-   Tell how much the function can adjust to the change in the dataset

 

### High Bias

\-   Over-simplified Model

\-   Under fitting

\-   High error on both test and train data

\-   Incorrect prediction

### High Variance

\-   Overly -complex Model

\-   Over-fitting

\-   Low error on train data and high on test

\-   Starts modelling the noise in the input

\-   Too specific model at given data

 

### Bias variance Trade-off

 

\-   Increase bias reduce variance and vice-versa

\-   Error = bias^2 + variance + irreducible error

\-   The best model is where the error is reduced

![image](https://user-images.githubusercontent.com/78076248/129868985-2fd63c24-7bff-4de3-8255-911ee93d0493.png)


Figure 1Bias-variance tradeoff cheat sheet — Image by author

![image](https://user-images.githubusercontent.com/78076248/129868997-315d17c9-a084-460e-b040-9a0677550778.png)


Figure 2 Bias-variance tradeoff cheat sheet — Image by author

 

### Question and answer

 

1. What is Bias in ML models?

\-   Bias in ML model is how much inaccurate the model’s prediction is. When a linear regression model tries to predict the total rental times per hour, the bias means how much the predicted rental times is far from the real total rental times 

2. What is Variance in ML models?

\-   Variance in ML model is how much hard the model can be used at other datasets. High variance means a model is overfitting to the given dataset. In other words, the model is to specified for the given dataset, so that prediction accuracy is high only in a given dataset.

3. What is the trade-off between bias and variance?

\-   Trade-off between bias and variance shows the negative correlation between bias and variance. When the bias increase, the variance decrease. On the other hand, when the bias decrease, the variance increase. When one of these are too high, the usability of model is low. Therefore, balancing spots found where the bias and variance are lowest.

4. How do you select the model (high bias or high variance) based on the training data size?

\-   High variance means that a model works well only in a given dataset. High bias means that a model’s prediction level is low. High variance lead to low bias, and low variance comes with high bias.

With a consideration of the trade-off between bias and variance, selections for high bias or high variance could be done. When the dataset is very large, high variance can be considered. Since the dataset is large, there is less chances of a model to use very different datasets. 

When a dataset is very small, on the other hand, variance should be low. Because a given dataset cannot represent the whole, model should not be overfitting. 


### Reference

https://medium.com/swlh/cheat-sheets-for-machine-learning-interview-topics-51c2bc2bab4f

 
