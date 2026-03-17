# Resume Classification Project

## Overview

This project is an AI-based Resume Classification System that categorizes resumes into different job roles such as React Developer, SQL Developer, Peoplesoft, and Workday using Natural Language Processing (NLP) and Machine Learning.

The project includes:
* Resume text extraction
* Exploratory Data Analysis (EDA)
* Feature extraction using TF-IDF vectorization
* Machine learning model training
* Web-based application for classification

---

## Repository Structure

Resume_Classification_Project

app.py / Resume_app1.py
Main application scripts used to run the resume classification service.

Model_Building_Final.ipynb
Notebook used for training and evaluating the machine learning model.

1. Text Extraction from Resume.ipynb
   Pipeline for extracting text from resume documents.

2. EDA Resume Classification.ipynb
   Exploratory Data Analysis for understanding the dataset.

Datasets/
Dataset folder containing:

* Resumes/
* Org_Resumes/
* Test Resumes/

ModelRFC.joblib
Trained Random Forest classification model.

VECTOR.joblib
Saved text vectorizer used for feature extraction.

skills.csv
Skills dataset used during preprocessing.

requirement.txt / Requirement1.txt
List of Python dependencies required to run the project.

Resume_Project_Setup_Steps.txt
Instructions for setting up and running the project.

---

## Setup

### 1. Clone the Repository

git clone https://github.com/your-username/Resume-Classification-Project.git

cd Resume-Classification-Project

---

### 2. Create Virtual Environment

python -m venv venv

Activate environment (Windows):

venv\Scripts\activate

Activate environment (Mac/Linux):

source venv/bin/activate

---

### 3. Install Dependencies

pip install -r requirement.txt

---

### 4. Verify Required Files

Make sure the following files exist:

* ModelRFC.joblib
* VECTOR.joblib
* Datasets folder
* Jupyter notebooks

---

## Usage

### Run the Web Application

python app.py

or

python Resume_app1.py

After running the script, open the local server URL shown in the terminal in your browser.
The system will classify the uploaded resume into a predicted job category.

---

### Use the Model Directly

Example Python code:

import joblib

model = joblib.load("ModelRFC.joblib")
vectorizer = joblib.load("VECTOR.joblib")

text = "Sample resume text"

prediction = model.predict(vectorizer.transform([text]))

print(prediction)

---

## Model Workflow

1. Resume text extraction
2. Data cleaning and preprocessing
3. Feature extraction using vectorization
4. Model training using Random Forest
5. Resume classification

---

## Notes

* Follow steps in Model_Building_Final.ipynb to retrain the model
* Ensure correct dataset paths before running scripts
* Adjust virtual environment commands based on your OS

---

## Author

Neha Dhurgude

---

## Future Improvements

* Improve accuracy using advanced NLP models like BERT
* Add more job categories
* Enhance UI/UX of the web application
* Deploy using cloud platforms (Render / AWS / Streamlit)

