# Predicting Public Sentiment on Vaccine Mandates Using KNN
This repository contains the project submitted for RSM8413: Machine Learning Analytics, where we used a K-Nearest Neighbors (KNN) model to predict public sentiment regarding a potential COVID-19 vaccine mandate. The model was developed to help the Government of Canada gauge support for such legislation without asking direct, divisive questions.

## Project Overview
In the context of the COVID-19 pandemic, the Government of Canada is exploring the possibility of enforcing a vaccine mandate for all adults. Our task was to develop a predictive model that can infer public support for a vaccine mandate based on a set of behavioral and demographic features, without directly asking the public about their stance on the mandate.

We achieved this through a KNN classification model that can predict whether an individual supports or opposes the mandate based on their responses to related questions.

## Dataset
The dataset, provided by the Institute of Global Health Innovation Imperial College London, includes over 6,000 survey responses from Canadians, with questions on:

Demographic details such as age and household size.
Behavioral aspects like mask usage and social distancing habits.
Sentiments towards the government’s handling of the pandemic and beliefs about vaccine efficacy.
Key features include:

age (Numeric)
gender (Binary)
household size (Numeric)
face mask usage, social event attendance, interaction with other households (Likert scales)
sentiment towards government handling and vaccine belief (Likert scales)
The target variable, vac_man_6, represents whether an individual supports a vaccine mandate for all adults (Yes/No).

## Methodology
### Data Cleaning & Processing
We preprocessed the data by:

Mapping categorical data: We converted Likert scale responses into numerical values for analysis.
Creating dummy variables for binary responses, such as gender and the target variable.
Handling missing values: Columns with missing or irrelevant data were removed, reducing the dataset to 6,170 valid observations.

### Model: K-Nearest Neighbors (KNN)
KNN was chosen due to its interpretability and effectiveness for classification tasks. Key steps:

Normalization: To avoid bias from varying feature scales, we applied Box-Cox transformation for skewed variables and Z-score normalization for normally distributed ones.
Cross-validation: We performed 10-fold cross-validation to identify the optimal value of k (number of neighbors).
Evaluation metrics: Accuracy, sensitivity, precision, and specificity were used to evaluate model performance.

## Results
After evaluating different values of k, the model demonstrated:

Accuracy: 65% when k=5.
Sensitivity: 63%—emphasized as the key metric, given the government's interest in identifying true supporters of the mandate.
Precision: 61%
These metrics allowed us to make informed decisions about public sentiment and how the government could frame policies regarding the vaccine mandate
