# Parkinson's Disease Prediction using Support Vector Machine (SVM)

## Project Overview
This project presents a machine learning solution for the early detection of Parkinson's Disease based on voice measurements. Utilizing a Support Vector Machine (SVM) classifier, the model is trained on a dataset containing various vocal feature parameters. The goal is to develop a robust predictive system that can assist in identifying individuals who may have Parkinson's Disease, contributing to early diagnosis and intervention.

## Project Description
Parkinson's Disease is a progressive neurodegenerative disorder that primarily affects dopamine-producing neurons in a specific area of the brain called the substantia nigra. Early detection is crucial for managing the disease and improving patients' quality of life. This project explores the use of voice analysis, a non-invasive and cost-effective method, to predict the presence of Parkinson's Disease. The SVM algorithm, known for its effectiveness in classification tasks, is employed to build a model that can distinguish between healthy individuals and those with Parkinson's based on their voice patterns.

The workflow includes data collection, exploratory data analysis, data preprocessing (including feature scaling), model training, and performance evaluation. A predictive system is then developed to make predictions on new, unseen data.

## Features
- **Data Loading and Initial Exploration**: Loading the dataset and examining its structure, including dimensions, column types, and basic statistics.
- **Handling Missing Values**: Verification that the dataset is complete and does not contain missing values.
- **Target Variable Distribution Analysis**: Understanding the distribution of Parkinson's positive and healthy cases within the dataset.
- **Feature-Target Separation**: Clearly defining features (independent variables) and the target variable (status).
- **Data Splitting**: Dividing the dataset into training and testing sets to ensure robust model evaluation.
- **Data Standardization**: Scaling numerical features using `StandardScaler` to prevent features with larger values from dominating the learning process.
- **Support Vector Machine (SVM) Classifier**: Implementation of an SVM with a linear kernel for classification.
- **Model Training**: Training the SVM model on the preprocessed training data.
- **Model Evaluation**: Assessing the model's performance using accuracy scores on both training and test datasets.
- **Predictive System**: A functional system capable of taking new voice feature inputs and predicting whether a person has Parkinson's Disease.

## Data Source
The dataset used in this project is `parkinsons.csv`, which contains various biomedical voice measurements from 195 individuals, 147 with Parkinson's and 48 healthy. The `status` column indicates the health status (1 for Parkinson's, 0 for healthy). Other columns represent different voice features such as fundamental frequency (Fo, Fhi, Flo), jitter, shimmer, HNR, RPDE, DFA, spread1, spread2, D2, and PPE.

## Data Preprocessing
1.  **Feature Selection**: The `name` column is dropped as it is an identifier and not relevant for model training. The `status` column is designated as the target variable.
2.  **Data Splitting**: The data is split into 80% for training and 20% for testing using `train_test_split` with a `random_state` for reproducibility.
3.  **Standardization**: Features are standardized using `StandardScaler`. This is a crucial step for SVMs, as they are sensitive to the scale of input features.

## Model Training
A Support Vector Machine (SVM) classifier with a linear kernel is chosen for this classification task. The model is trained on the standardized training data (`x_train`, `y_train`).

## Model Evaluation
The performance of the trained SVM model is evaluated using the accuracy score.
-   **Training Data Accuracy**: Measures how well the model performs on the data it was trained on.
-   **Test Data Accuracy**: Measures the model's generalization capability on unseen data.

## Technologies Used
-   **Python**: Programming language.
-   **NumPy**: For numerical operations, especially with arrays.
-   **Pandas**: For data manipulation and analysis.
-   **Scikit-learn (sklearn)**: For machine learning algorithms, including `StandardScaler`, `train_test_split`, `svm.SVC`, and `accuracy_score`.

## Installation
To get started with this project, ensure you have Python installed. Then, install the required libraries using pip:

```bash
pip install numpy pandas scikit-learn
```
