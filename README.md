# ML-healthcare_premium-Prediction-Regression
Project Overview
This project involves predicting health care premiums based on various features using machine learning regression techniques. The goal is to develop a model that can accurately predict the annual premium amount a person should pay, based on their demographic and health-related information.

Features
The dataset includes the following features:

age: Age of the individual.
gender: Gender of the individual (Male, Female).
region: Geographic region (Northeast, Northwest, Southeast, Southwest).
marital_status: Marital status (Unmarried, Married).
number_of_dependants: Number of dependents.
bmi_category: Body Mass Index category (Overweight, Underweight, Normal, Obesity).
smoking_status: Smoking status (Regular, No Smoking, Occasional, Smoking=0, Does Not Smoke, Not Smoking).
employment_status: Employment status (Self-Employed, Freelancer, Salaried).
income_level: Income level categorized as per income brackets (> 40L, <10L, 10L - 25L, 25L - 40L).
income_lakhs: Actual income in lakhs.
medical_history: Medical history including various diseases (e.g., Diabetes, High blood pressure).
insurance_plan: Type of insurance plan (Bronze, Silver, Gold).
annual_premium_amount: Target variable - the annual premium amount to be predicted.
genetical_risk: Genetical risk score.
Data Preprocessing
Handling Categorical Variables: Categorical variables such as gender, region, and smoking status are encoded into numerical values. For instance, the insurance plan is encoded as Bronze=1, Silver=2, Gold=3.

Medical History Processing: Medical history is split into multiple diseases, and each disease is converted to lowercase. Risk scores are assigned based on predefined values for each disease.

Normalization: Risk scores are normalized to ensure consistent scaling of the data.

Scaling: The data is scaled based on age using different scalers for individuals <= 25 years and those > 25 years.

Machine Learning Model
The project uses regression algorithms to predict the annual premium amount. Key steps include:

Feature Engineering: Create features based on the given data, including one-hot encoding for categorical variables and calculating risk scores.

Model Training: Train various regression models (e.g., Linear Regression, Random Forest Regressor) to predict the annual premium amount based on the processed features.

Model Evaluation: Evaluate the performance of the models using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared.

Streamlit Application
A Streamlit application is developed to provide an interactive interface for users to input their data and get predictions. The application allows users to:

Input personal and health-related information.
Receive predictions for the annual premium amount based on their inputs.
File Structure
data/: Contains datasets used for training and testing.
src/: Contains Python scripts for data preprocessing, model training, and evaluation.
app/: Contains the Streamlit application files.
models/: Contains saved models and scalers.
notebooks/: Contains Jupyter notebooks for exploratory data analysis and model prototyping.
requirements.txt: Lists the Python packages required for the project.
README.md: This file.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/ML-healthcare_premium-Prediction-Regression.git
cd ML-healthcare_premium-Prediction-Regression
#Install required packages:

pip install -r requirements.txt
# Run the Streamlit application:

bash
Copy code
streamlit run app/app.py
Contributing
Feel free to contribute to the project by opening issues or submitting pull requests. Ensure that you follow the project's code of conduct and contribution guidelines.

License
This project is licensed under the MIT License. See the LICENSE file for details.
