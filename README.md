# Feature Finder


## NON-TECHNICAL EXPLANATION
This project utilizes the Kaggle Machine Learning & Data Science Survey to power a predictive model that informs both new and existing survey respondents about actionable changes they can make to enhance their job satisfaction, considering their unchangeable circumstances. By analyzing survey data, the model identifies key factors under a respondent's control that can positively impact their job satisfaction. This tool is particularly useful for individuals seeking to understand how specific changes in their professional lives could lead to greater satisfaction at work.

## DATA
The dataset, created and maintained by Kaggle in collaboration with The Pudding, comprises 16,716 survey responses from the global data science and machine learning community. It was collected from August 7th to August 25th to provide a comprehensive view of the field across various industries. The data includes multiple choice and anonymized freeform responses, with preprocessing steps such as standardization of currency values to USD and conversion of categorical data into numerical format to facilitate machine learning analysis. This dataset is publicly available on Kaggle for analysis and educational purposes, adhering to Kaggle's terms of use.

## MODEL 
The model employed in this project is a neural network specifically designed for predicting job satisfaction, named JobSatisfactionNN. It consists of three fully connected layers with ReLU activations and incorporates dropout layers after each activation to mitigate overfitting. Dropout rates are set at 50% for both hidden layers. Additionally, the model uses weight decay in the Adam optimizer as a form of regularization to further prevent overfitting. To ensure robustness and generalizability of the model, k-fold validation was utilized to evaluate performance across different subsets of the data. Early stopping was also implemented; training halts if there is no improvement in validation loss after a specified number of epochs (patience parameter), ensuring that the model does not overfit to the training data. These strategies collectively enhance the model's ability to generalize to new, unseen data while maintaining a balance between bias and variance.

## HYPERPARAMETER OPTIMSATION
In the training configuration of the JobSatisfactionNN model, several hyperparameters were carefully selected and optimized to achieve the best performance. The primary hyperparameters include the learning rate, batch size, and the number of epochs. A learning rate of 0.0005 was chosen to ensure that the model converges smoothly without overshooting the minimum of the loss function. The batch size was set to 32, balancing the need for computational efficiency and the benefit of stochastic gradient descent's noise in escaping local minima. The model was initially set to train for 500 epochs, but with early stopping implemented, training could cease earlier if the validation loss does not improve, preventing unnecessary computations and overfitting. The weight decay parameter in the Adam optimizer was also tuned to 0.0001 as a regularization term to reduce overfitting further. These hyperparameters were likely chosen based on empirical testing and validation performance, ensuring that the model achieves a good balance between accuracy and generalization.

## RESULTS
The JobSatisfactionNN model has demonstrated its capability to predict job satisfaction levels with a final training loss of 0.6257, a validation loss of 0.8106, and a test loss of 0.8644. Through sensitivity analysis, the model identifies which actionable features, when altered, could significantly improve an individual's job satisfaction. This analysis allows respondents to understand which changes in their responses could lead to improved job satisfaction, focusing on factors they can influence despite the constraints of their unchangeable circumstances. This insight is invaluable for guiding personal and professional development decisions aimed at enhancing job satisfaction.

'The most impactful change for improving job satisfaction is transitioning from the original "No" remote work policy to the new "Yes" remote work policy, which resulted in an increase of 0.4280 in job satisfaction, from an initial level of -0.2621 to an updated level of 0.1659'

CONTACT DETAILS
george@featuringyou.ai 

