🩺 Disease Prediction Model (Local Version with File Picker)

This project implements a Disease Prediction System using Machine Learning (Random Forest Classifier).
It allows users to upload a CSV dataset of disease symptoms and patient details, preprocess the data, train a model, evaluate its performance, and make predictions for new cases.

📌 Features

CSV File Picker (Tkinter): Easily select your dataset interactively.

Preprocessing: Automatic encoding of categorical variables like Fever, Cough, Blood Pressure, etc.

Model Training: Uses Random Forest Classifier.

Evaluation Metrics: Accuracy, Precision, Recall, F1 Score.

Prediction Function: Make predictions on new patient data.

⚙️ Installation

Install the required Python libraries:

pip install pandas scikit-learn


Tkinter is pre-installed with most Python distributions.

📊 Dataset Format

Your CSV should include columns like:

Disease

Fever

Cough

Fatigue

Difficulty Breathing

Age

Gender

Blood Pressure

Cholesterol Level

Outcome Variable (target)

Example row:

Disease,Fever,Cough,Fatigue,Difficulty Breathing,Age,Gender,Blood Pressure,Cholesterol Level,Outcome Variable
Influenza,Yes,No,Yes,Yes,20,Female,Low,Normal,Positive

🧠 Model Workflow

Load CSV Dataset
Select dataset using a Tkinter file picker.

Preprocess Data

Encode categorical values using LabelEncoder.

Split dataset into features X and target y.

Train Model
Train using RandomForestClassifier.

Evaluate Model
Calculate Accuracy, Precision, Recall, F1 Score.

Make Predictions
Predict disease outcome for new patient data.

🚀 Example Usage

Prediction on New Data:

sample1 = {
    'Disease': 'Influenza',
    'Fever': 'Yes',
    'Cough': 'No',
    'Fatigue': 'Yes',
    'Difficulty Breathing': 'Yes',
    'Age': 20,
    'Gender': 'Female',
    'Blood Pressure': 'Low',
    'Cholesterol Level': 'Normal'
}

print(f"Prediction for sample1: {make_prediction(sample1)}")


Output:

Prediction for sample1: Positive