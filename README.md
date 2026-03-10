# Phishing Website Detection Using Machine Learning

## Project Overview
Phishing is a type of cyber attack where fraudulent websites attempt to steal sensitive information such as login credentials, banking details, or personal data. Traditional blacklist-based systems struggle to detect newly created phishing websites.

This project uses **Machine Learning** to automatically classify websites as **phishing or legitimate** based on various website characteristics.

The system analyzes **URL-based, domain-based, and content-based features** to detect suspicious patterns and improve cybersecurity protection.

---

## Problem Statement
Phishing attacks are increasing rapidly and pose serious risks including:

- Identity theft  
- Financial fraud  
- Data breaches  

Since phishing websites are often short-lived, traditional security systems cannot detect them efficiently. Machine Learning helps identify hidden patterns and classify websites automatically.

---

## Dataset Overview

The dataset contains **30 features** that describe characteristics of a a website along with a **target label**.

Target Variable:

- **Result = -1 → Phishing Website**
- **Result = 1 → Legitimate Website**

Feature categories include:

### URL-Based Features
- Having IP Address
- URL Length
- Shortening Service
- Having @ Symbol
- Double Slash Redirecting
- Prefix/Suffix

### Domain-Based Features
- SSL Final State
- Domain Registration Length
- DNS Record
- Age of Domain
- Page Rank

### Content-Based Features
- Request URL
- URL of Anchor
- Links in Tags
- Iframe
- Pop-up Window
- Right Click Disabled

These features help identify suspicious behavior commonly used in phishing websites.

---

## Technologies Used

### Data Processing & Machine Learning
- Python  
- Scikit-learn  
- XGBoost  
- imbalanced-learn  
- Pandas  
- NumPy  

### Data Visualization
- Matplotlib  
- Seaborn  

### Web Development
- Flask  
- Jinja2  
- Werkzeug  

### Deployment & Cloud
- AWS (S3 / EC2)  
- boto3  
- python-dotenv  

### Monitoring
- Evidently

---

## Project Workflow

### 1. Data Collection
Loaded phishing website dataset containing 30 features.

### 2. Data Preprocessing
- Handled missing values  
- Converted categorical values  
- Normalized feature values  
- Split data into training and testing sets  

### 3. Model Training
Trained multiple classification models:

- Logistic Regression  
- Random Forest  
- Support Vector Machine (SVM)  
- XGBoost  

### 4. Model Evaluation
Models were evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  

### 5. Model Deployment
- Best performing model deployed using **Flask API**
- Integrated with frontend interface
- Designed for **cloud deployment using AWS**

---

## Machine Learning Models Used

| Model | Purpose |
|------|------|
| Logistic Regression | Baseline classification model |
| Random Forest | Ensemble model handling complex feature interactions |
| Support Vector Machine | Effective for high-dimensional classification |
| XGBoost | High-performance gradient boosting algorithm |

Random Forest and XGBoost showed the best performance in detecting phishing websites.

---

## Model Evaluation Metrics

To measure the performance of the models, the following metrics were used:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

These metrics help evaluate the model's ability to correctly detect phishing websites while minimizing false predictions.

---

## Deployment

The trained model is deployed using **Flask** to create an API that allows users to check whether a website is phishing or legitimate.

Deployment components include:

- Flask web application
- Model serialization using `dill`
- Environment management using `.env`
- Cloud integration with **AWS**

Users can input a website URL and receive a prediction result.

---

## Project Structure

```
Phishing-Website-Detection
│
├── data
│   └── phishing_dataset.csv
│
├── notebooks
│   └── EDA_and_Model_Training.ipynb
│
├── src
│   ├── data_preprocessing.py
│   ├── model_training.py
│   ├── prediction_pipeline.py
│
├── app.py
├── requirements.txt
├── README.md
```

---

## Key Learnings

- Feature engineering for cybersecurity datasets
- Handling imbalanced datasets using `imblearn`
- Comparing multiple ML classification models
- Building ML APIs using Flask
- Deploying machine learning applications to cloud platforms

---

## Future Improvements

- Real-time phishing detection using live URL analysis  
- Browser extension integration  
- Deep learning based phishing detection  
- Continuous model monitoring using Evidently  

---

GitHub:  
https://github.com/SoumenB45

LinkedIn:  
https://www.linkedin.com/in/soumen-baidya/
