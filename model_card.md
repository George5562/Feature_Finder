Model Card

Model Description

Input: The model takes as input the responses from the 2017 Kaggle Machine Learning & Data Science Survey. These responses include various features such as demographics, education level, employment status, and specific answers related to job satisfaction.

Output: The primary output of the model is the prediction of job satisfaction levels among survey respondents. Additionally, the model performs a sensitivity analysis to determine which factors respondents can change to potentially improve their job satisfaction, based on the given fixed responses.

Model Architecture: The model architecture defined in the notebook is a neural network specifically designed for predicting job satisfaction. It is implemented using PyTorch's nn.Module. The network consists of three fully connected (linear) layers. The first layer takes an input of dimension equal to the number of features in the dataset and outputs 128 nodes. This is followed by a dropout layer with a dropout rate of 0.5 to prevent overfitting. The second layer reduces the dimension from 128 to 64 nodes, followed by another dropout layer with the same dropout rate. The final layer is a single-node output layer that outputs the predicted job satisfaction. Activation functions used are ReLU for the hidden layers.  The model also incorporates early stopping based on validation loss to further mitigate overfitting.

The script in analysis.ipynb processes job satisfaction data, categorizes features, scales numerical data, and utilizes a neural network model to predict job satisfaction. It defines and loads a pre-trained neural network model, performs sensitivity analysis to identify the most impactful changes to actionable features that could improve job satisfaction, and finally, uses these insights to generate human-readable outputs. The sensitivity analysis explores how changes in both numerical and binary actionable features affect the predicted job satisfaction, helping to pinpoint specific adjustments that could lead to significant improvements.

Performance

Key performance results:
- Early stopping was implemented at epoch 108.
- Final Training Loss: 0.6257
- Final Validation Loss: 0.8106
- Test Loss: 0.8644

Limitations
The model's predictions are only as good as the data it is trained on; biases in the survey responses could affect the results. Additionally, there were a significant number of blanks in the survey responses, leading to assumptions being made during data preprocessing.
Sensitivity analysis assumes model linearity and independence between features, which may not always hold true.
The model's applicability is limited to scenarios and data distributions similar to those of the Kaggle 2017 survey.

Trade-offs
There might be a trade-off between model complexity and interpretability, especially when using sophisticated models for prediction.
Sensitivity analysis can be computationally expensive, impacting the efficiency of the model when dealing with large datasets or in real-time applications.
The model may perform well on average but could have lower performance for certain subgroups within the data.
