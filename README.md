# 🤖 Automated Machine Learning using IBM AutoAI

[![IBM Watson](https://img.shields.io/badge/IBM-Watson%20Studio-blue?logo=ibm)](https://www.ibm.com/cloud/watson-studio)
[![AutoAI](https://img.shields.io/badge/AutoAI-Enabled-brightgreen)](https://www.ibm.com/cloud/watson-studio/autoai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Built a machine learning model using **IBM Watson Studio AutoAI** to automate the end-to-end ML pipeline — from data preprocessing to model deployment — with minimal manual effort.

---

## 📝 Project Summary

- ✅ Built a machine learning model using **IBM Watson Studio AutoAI** to automate the end-to-end ML pipeline
- ✅ Performed automated **data preprocessing**, **feature engineering**, and **model selection**
- ✅ Compared multiple algorithms and selected the best-performing model based on evaluation metrics
- ✅ Generated **optimized pipelines** and deployed the model using **AutoAI API**
- ✅ Utilized **Python integration** for model testing and predictions

---

## 📌 What is AutoAI?

**AutoAI** is an automated machine learning (AutoML) capability in IBM Watson Studio. It removes the complexity of building ML pipelines by automatically:

- Cleaning and preprocessing raw data
- Engineering the most relevant features
- Selecting the best algorithms
- Tuning hyperparameters
- Ranking candidate models (pipelines) by performance

The output is a fully optimized, deployment-ready ML pipeline.

---

## 🚀 Key Features

| Feature | Description |
|---|---|
| ⚙️ **Automated Data Preparation** | Handles missing values, encoding, and scaling automatically |
| 🔍 **Feature Engineering** | Selects and transforms features to maximize model accuracy |
| 🧠 **Algorithm Selection** | Evaluates multiple ML algorithms (Random Forest, XGBoost, etc.) |
| 📊 **Pipeline Comparison** | Ranks top pipelines by metrics like accuracy, AUC, F1-score |
| 🚀 **Model Deployment** | Deploy the best pipeline to IBM Watson Machine Learning with one click |
| 🐍 **Python Code Export** | Export the generated pipeline as Python code for further customization |
| 📁 **Notebook Integration** | Save any pipeline as a Jupyter Notebook for deeper analysis |

---

## 🗂️ Repository Contents

```
AutoAI/
│
├── README.md                          # Project overview and documentation
└── Watson Machine learning Steps.pdf  # Step-by-step guide for AutoAI setup
```

---

## 🛠️ How to Use AutoAI – Step-by-Step

### Prerequisites
- An active [IBM Cloud account](https://cloud.ibm.com/registration)
- IBM Watson Studio instance provisioned
- IBM Watson Machine Learning service instance

### Steps

1. **Login to IBM Cloud** → Navigate to **Watson Studio**
2. **Create a Project** → Click *New Project* → Select *Create an empty project*
3. **Add your Dataset** → Upload a CSV file as a data asset
4. **Launch AutoAI** → Click *Add to Project* → Select *AutoAI Experiment*
5. **Configure the Experiment**:
   - Select your dataset
   - Choose the **prediction column** (target variable)
   - Select prediction type: *Binary Classification*, *Multiclass*, or *Regression*
6. **Run the Experiment** → AutoAI generates and ranks multiple pipelines
7. **Review Pipelines** → Compare leaderboard results and view feature importance
8. **Save & Deploy** → Save the best pipeline as a model and deploy to WML
9. **Test the Endpoint** → Use the deployment's REST API to make predictions
10. **Export Code** → Optionally export the pipeline as a Python notebook

> 📄 For a detailed visual guide, see **[Watson Machine Learning Steps.pdf](Watson%20Machine%20learning%20Steps.pdf)**

---

## 📈 AutoAI Pipeline Overview

```
Raw Dataset
    │
    ▼
Data Preprocessing  ──► Handle nulls, encode categoricals, normalize
    │
    ▼
Feature Engineering ──► Transform, combine, and select best features
    │
    ▼
Algorithm Selection ──► Try Random Forest, XGBoost, LightGBM, etc.
    │
    ▼
Hyperparameter Opt. ──► Tune each algorithm's parameters
    │
    ▼
Pipeline Leaderboard ──► Rank top-performing pipelines
    │
    ▼
Model Deployment    ──► Deploy via IBM Watson Machine Learning
```

---

## 🧪 Supported Model Types

- **Binary Classification** – e.g., churn prediction, fraud detection
- **Multiclass Classification** – e.g., category prediction
- **Regression** – e.g., price prediction, demand forecasting

---

## 🌐 Deployment & API Integration

Once deployed via Watson Machine Learning, you can integrate the model into any application using the REST API:

```python
import requests

# IBM Watson ML scoring endpoint
url = "https://<region>.ml.cloud.ibm.com/ml/v4/deployments/<deployment_id>/predictions"
headers = {
    "Authorization": "Bearer <YOUR_IAM_TOKEN>",
    "Content-Type": "application/json"
}
payload = {
    "input_data": [{
        "fields": ["feature1", "feature2", "feature3"],
        "values": [[value1, value2, value3]]
    }]
}
response = requests.post(url, json=payload, headers=headers)
print(response.json())
```

---

## 📚 Resources

- 📖 [IBM AutoAI Documentation](https://www.ibm.com/docs/en/watson-studio?topic=models-autoai)
- 🎓 [IBM AutoAI Tutorial](https://developer.ibm.com/tutorials/automate-model-building-with-autoai/)
- 🔗 [IBM Watson Studio](https://www.ibm.com/cloud/watson-studio)
- 💡 [IBM Cloud Free Tier](https://www.ibm.com/cloud/free)

---

## 👤 Author

**Jaya Shukla**  
🔗 [GitHub](https://github.com/shuklajaya337)

---

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
