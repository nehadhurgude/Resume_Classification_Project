# Resume Classification Project

## Overview

This project classifies resumes into different job profiles such as React Developer, SQL Developer, Peoplesoft, and Workday using Natural Language Processing (NLP) and Machine Learning.

The project includes:

* Resume text extraction
* Exploratory data analysis (EDA)
* Feature extraction using vectorization
* Machine learning model training
* A web application for resume classification

---

## Project Screenshots

### Dashboard
![WhatsApp Image 2026-03-16 at 10 49 15 PM](https://github.com/user-attachments/assets/465382fd-736f-46c8-a601-643e20744b0d)

### Data Preview
![WhatsApp Image 2026-03-16 at 10 49 48 PM](https://github.com/user-attachments/assets/2420d9bb-081d-44e0-8a42-9e12403fd06f)


### Model Prediction
![WhatsApp Image 2026-03-16 at 10 51 20 PM](https://github.com/user-attachments/assets/91984506-58ae-44e4-b1a1-73b09120f936)
![WhatsApp Image 2026-03-16 at 10 51 47 PM](https://github.com/user-attachments/assets/dfb800b1-b2ae-413e-b04f-c9d724c7cc8d)
![WhatsApp Image 2026-03-16 at 10 52 36 PM](https://github.com/user-attachments/assets/9452249e-64e3-47c5-bdd2-4c55d5f1dbee)


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

* If training the model again, follow the steps in **Model_Building_Final.ipynb**.
* Ensure dataset paths in the scripts match your folder structure.
* If using Mac or Linux, adjust the virtual environment activation commands accordingly.

---

## Author

Tanvi Powar

---

## Future Improvements

* Improve classification accuracy with advanced NLP techniques
* Add more job categories
* Deploy the application using Streamlit or Flask

