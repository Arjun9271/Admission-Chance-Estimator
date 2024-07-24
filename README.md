# 🎓 Admission Prediction System

This project aims to predict the probability of a student's admission into a university based on various factors such as GRE Score, TOEFL Score, University Rating, SOP, LOR, CGPA, and Research experience. The project involves data cleaning, exploratory data analysis, and the application of multiple regression models to achieve the best predictive performance.

## 📁 Project Structure

- **Data Loading**: Load the dataset from a CSV file.
- **Data Understanding**: Initial inspection of the dataset to understand its structure and contents.
- **Data Cleaning**: Clean the dataset by renaming columns, handling missing values, and removing unnecessary columns.
- **Exploratory Data Analysis (EDA)**: Perform EDA to understand the relationships between different variables.
- **Data Preparation**: Prepare the data for modeling by encoding categorical variables.
- **Modeling**: Apply various regression models to predict the chance of admission.
- **Model Evaluation**: Evaluate the performance of the models using appropriate metrics.

## 🚀 Getting Started

### 📥 Prerequisites

To run this project, you will need to have Python installed along with the necessary libraries such as pandas, numpy, seaborn, matplotlib, scikit-learn, and pickle.

### 📂 Data Loading

The dataset is loaded into a pandas DataFrame for ease of manipulation and analysis. The dataset contains the following columns:
- **Serial No.**: Unique identifier for each record.
- **GRE Score**: GRE scores of the students.
- **TOEFL Score**: TOEFL scores of the students.
- **University Rating**: Rating of the university.
- **SOP**: Strength of Statement of Purpose.
- **LOR**: Strength of Letter of Recommendation.
- **CGPA**: Undergraduate GPA.
- **Research**: Whether the student has research experience (1 for Yes, 0 for No).
- **Chance of Admit**: Probability of admission.

### 🔍 Data Understanding

Initial data exploration is done to inspect the first few rows of the dataset and understand the structure and contents. Columns are renamed for better readability, and the `Research` column is converted from numeric to categorical format ('yes' and 'no').

### 🔢 Data Cleaning

- Dropping unnecessary columns (e.g., `Serial No.`).
- Checking for and handling missing values (none found in this dataset).
- Checking for duplicate entries (none found in this dataset).

### 📊 Exploratory Data Analysis (EDA)

- **Correlation Analysis**: A heatmap is used to visualize the correlation between different variables.
- **Histograms and KDE Plots**: Histograms and Kernel Density Estimation (KDE) plots are created for continuous variables to understand their distributions.
- **Box Plots**: Box plots are created to identify any potential outliers in the continuous variables.
- **Pie Chart**: A pie chart is created to visualize the proportion of students with and without research experience.

### 🛠️ Data Preparation

- Encoding the `Research` column from categorical ('yes' and 'no') to numeric (1 and 0).

### 🏋️‍♂️ Modeling

Several regression models are applied to predict the chance of admission:

1. **Linear Regression**:
   - A basic linear regression model is trained on the dataset.
   - The model is evaluated using the R-squared metric for both training and test datasets.
   - Cross-validation is performed to assess the model's performance.

2. **Polynomial Regression**:
   - Polynomial features are generated to capture non-linear relationships.
   - A linear regression model is trained on the polynomial features.
   - The model is evaluated using the R-squared metric and cross-validation.

3. **Lasso Regression**:
   - Lasso regression is applied for feature selection and regularization.
   - Hyperparameter tuning is performed using GridSearchCV.
   - The model is evaluated using the R-squared metric and cross-validation.

4. **Ridge Regression**:
   - Ridge regression is applied for regularization.
   - Hyperparameter tuning is performed using GridSearchCV.
   - The model is evaluated using the R-squared metric and cross-validation.

5. **ElasticNet Regression**:
   - ElasticNet regression combines Lasso and Ridge regularizations.
   - Hyperparameter tuning is performed using GridSearchCV.
   - The model is evaluated using the R-squared metric and cross-validation.

### 📈 Model Evaluation

The performance of each model is evaluated using the R-squared metric for both training and test datasets. Cross-validation is also performed to assess the model's generalizability. Based on the results, the Multiple Linear Regression model provided the best performance.

---

This README provides a comprehensive overview of the project, explaining the data, processes, and methodologies used to build and evaluate the admission prediction system.
