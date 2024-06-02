# Datasheet Template

## Motivation

- The dataset was created to establish a comprehensive view of the state of data science and machine learning across industries, based on a survey conducted by Kaggle.
- The dataset was created by Kaggle, in collaboration with The Pudding for the interactive report.

## Composition

- The instances in the dataset represent survey responses from individuals in the field of data science and machine learning.
- There are 16,716 instances (respondents).
- The dataset includes multiple choice responses, freeform text responses, and currency conversion rates, although freeform responses were not used for this model.
- The dataset contains data that might be considered confidential as it includes individual responses to survey questions, although care has been taken to anonymize the data.

## Collection process

- The data was acquired through a survey conducted by Kaggle.
- The survey targeted the global community of data scientists and was not a sample of a larger subset.
- The survey was conducted from August 7th to August 25th.

## Preprocessing/cleaning/labelling

- During the preprocessing phase, each column of the dataset was meticulously reviewed to assess its relevance and determine appropriate methods for handling missing values. For instance, blanks in the dataset were replaced using statistically relevant methods tailored to the nature of the data in each column.
- Currency values were standardized to USD to maintain consistency across financial data. Responses to multiple choice questions were quantified where possible, converting categorical data into numerical format to facilitate analysis. This conversion aids in applying machine learning algorithms more effectively.
- Each column was categorized into one of three labels: 'Fixed', 'Actionable', or 'Outcome', to assist in subsequent analyses and model training processes.
- The separation of multiple choice and freeform responses, along with the randomization of freeform responses across columns, was implemented to ensure the anonymity of the respondents.
- The documentation does not clarify whether the original "raw" data was preserved post-preprocessing or if only the modified dataset was retained.

## Uses

This dataset is structured to support advanced analytical models, particularly those aimed at understanding and predicting various 'Outcome' variables identified during the preprocessing phase. Each 'Outcome' variable represents a potential target for predictive modeling, which can be leveraged to assess the impact of various factors on these outcomes.

For instance, a machine learning model can be trained on any of the 'Outcome' variables to predict specific results based on the input features. After training, sensitivity analysis can be applied to the model. This analysis helps in identifying which 'Actionable' variables, when altered, could have the most significant influence on the predicted outcome for an individual respondent.

This approach allows researchers and analysts to not only predict outcomes but also to understand which levers can be adjusted to drive improvements in those outcomes. This is particularly useful in scenarios where strategic interventions are considered to optimize individual or group performance based on the model's insights.

The practical application of this dataset, combined with sensitivity analysis, provides a powerful tool for decision-makers looking to implement data-driven strategies that can significantly impact the modeled outcomes.


## Distribution

- The dataset has been shared publicly on Kaggle, along with the kernels used in the report.
- The dataset is subject to Kaggle's terms of use and may be used freely for analysis and educational purposes, but with restrictions on attempts to identify individual respondents.

## Maintenance

- The dataset is maintained by Kaggle.

