# 🏦 Customer Churn Prediction — ANN + Streamlit

A deep learning web application that predicts whether a bank customer is likely to churn, built using an Artificial Neural Network (ANN) trained on real banking data and deployed with Streamlit.

![Python](https://img.shields.io/badge/Python-3.13-blue?style=flat&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat&logo=tensorflow)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red?style=flat&logo=streamlit)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Preprocessing-blue?style=flat&logo=scikitlearn)

---

## 📌 Project Overview

Customer churn is one of the most critical problems in the banking industry. This project builds an end-to-end ML pipeline that:

- Trains an ANN model on 10,000+ customer records
- Predicts churn probability for individual customers
- Provides an interactive Streamlit UI for real-time predictions

---

## 🖥️ App Demo

<img width="1920" height="1000" alt="image" src="https://github.com/user-attachments/assets/fa5eb37d-2066-4b57-988f-de0aed4e019e" />



The app takes customer inputs like Geography, Age, Balance, Credit Score, and predicts:
- **Churn Probability** (0.00 – 1.00)
- **Final Verdict** — Likely to churn or not

---

## 🗂️ Project Structure

```
├── app.py                        # Streamlit web application
├── experiments.ipynb             # Model training and experimentation
├── hyperparametertuninggann.ipynb # Hyperparameter tuning with Keras Tuner
├── prediction.ipynb              # Prediction pipeline notebook
├── model.h5                      # Trained ANN model
├── scaler.pkl                    # StandardScaler for feature scaling
├── label_encoder.pkl             # LabelEncoder for Gender
├── onehot_encoder_geo.pkl        # OneHotEncoder for Geography
├── Churn_Modelling.csv           # Dataset
└── requirements.txt              # Dependencies
```

---
## 🏋️ Model Training

The model was trained for 100 epochs with early stopping on 8,000 customer records.

**Sample Training Log:**
Epoch 16/100
250/250 ━━━━━━━━━━━━━━━━━━━━ 0s 2ms/step

accuracy: 0.8774
loss: 0.3002
val_accuracy: 0.8605
val_loss: 0.3448

**Final Results:**
| Metric | Score |
|---|---|
| Training Accuracy | 87.74% |
| Validation Accuracy | 86.05% |
| Training Loss | 0.30   |
| Validation Loss | 0.34 |

**Key Observations:**
- Small gap between training and validation accuracy confirms **no overfitting**
- Model generalizes well to unseen customer data
- Each epoch completed in under 1 second
---

## 🧠 Model Architecture

| Layer | Type | Units | Activation |
|---|---|---|---|
| Input | Dense | 64 | ReLU |
| Hidden | Dense | 32 | ReLU |
| Output | Dense | 1 | Sigmoid |

- **Loss Function:** Binary Crossentropy
- **Optimizer:** Adam
- **Epochs:** 100 with Early Stopping
- **Dataset:** 10,000 customer records, 12 features

---

## 📊 Features Used

| Feature | Description |
|---|---|
| CreditScore | Customer's credit score |
| Geography | Country (France / Germany / Spain) |
| Gender | Male / Female |
| Age | Customer age |
| Tenure | Years with the bank |
| Balance | Account balance |
| NumOfProducts | Number of bank products used |
| HasCrCard | Has credit card (0/1) |
| IsActiveMember | Active member status (0/1) |
| EstimatedSalary | Estimated annual salary |

---

## ⚙️ Tech Stack

- **Deep Learning:** TensorFlow, Keras
- **Data Processing:** Pandas, NumPy, scikit-learn
- **Visualization:** Matplotlib, Seaborn
- **Web App:** Streamlit
- **Model Persistence:** Pickle, HDF5 (.h5)

---

## 🚀 Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/Deebyendu/ANN-Classification-Churn.git
cd ANN-Classification-Churn
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the Streamlit app**
```bash
streamlit run app.py
```

---

## 📈 Results

- The model successfully classifies customers at risk of churning
- Hyperparameter tuning notebook included for performance optimization
- Prediction pipeline notebook demonstrates end-to-end inference

---

## 🙋‍♂️ Author

**Deebyendu Mondal**
- 🔗 [LinkedIn](https://www.linkedin.com/in/deebyendu-mondal-879248238/)
- 🐙 [GitHub](https://github.com/Deebyendu)
- 📧 deebyendumondal@gmail.com
