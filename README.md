# NIROG

# Health Prediction Web Application

This web application helps users predict their health risks for diabetes and heart attacks based on input data. It also provides a Diabetes Pedigree Function (DPF) calculation. The app is built with Flask and uses machine learning models to make predictions.

## Features

- **Diabetes Risk Prediction**: Users can input health metrics such as glucose level, blood pressure, BMI, diabetes pedigree function, and age to predict their diabetes risk.
- **Heart Attack Risk Prediction**: Allows users to assess their heart attack risk based on metrics like age, sex, cholesterol, blood pressure, heart rate, and lifestyle factors (e.g., smoking, obesity).
- **Diabetes Pedigree Function Calculation**: Computes a DPF score based on family history of diabetes and age at diagnosis.
- **Personalized Health Recommendations**: Based on prediction outcomes, users receive lifestyle and health recommendations tailored to their risk levels.

## Installation

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Dependencies**
   Ensure you have Python installed, then install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Prepare Datasets**
   Place your dataset files (e.g., `diabetes.csv` and `heart_attack_dataset.csv`) in the `Nirog/Datasets` folder.

4. **Run the Application**
   Start the Flask server:
   ```bash
   python app.py
   ```
   By default, the application will be accessible at `http://127.0.0.1:5000`.

## Usage

1. **Home Page**: Navigate to the main page to access different prediction tools.
2. **Diabetes Prediction**: Input relevant health metrics to predict diabetes risk.
3. **Heart Attack Prediction**: Enter cardiovascular and lifestyle data to predict heart attack risk.
4. **DPF Calculation**: Input family history data to calculate the Diabetes Pedigree Function score.

## Application Routes

- `/`: Home page.
- `/diabeteshtml`: Page for entering data for diabetes prediction.
- `/hearthtml`: Page for entering data for heart attack prediction.
- `/dpfhtml`: Page for calculating the Diabetes Pedigree Function.
- `/diabetespredict`: Endpoint for making a diabetes prediction.
- `/heartpredict`: Endpoint for making a heart attack prediction.
- `/dpf_predict`: Endpoint for calculating the Diabetes Pedigree Function.

## Machine Learning Models

- **Diabetes Prediction**: Uses a K-Nearest Neighbors (KNN) model with selected health metrics to predict diabetes risk.
- **Heart Attack Prediction**: Another KNN model is trained on heart attack risk factors for prediction.
- **Recommendations**: Based on the probability of risk, personalized recommendations are provided to users in categories such as low, moderate, high, and very high risk.

