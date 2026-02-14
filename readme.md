# 🔥 Algerian Forest Fire Weather Index (FWI) Prediction – End-to-End ML Project

This project is a **complete end-to-end Machine Learning application** that predicts the **Fire Weather Index (FWI)** using meteorological and environmental features from the **Algerian Forest Fires dataset**.
The trained model is deployed using a **Flask web application** where users can input parameters and get real-time predictions.

---

## 📌 Project Overview

Forest fires pose a serious environmental and economic threat.
This project leverages **machine learning (Ridge Regression)** to predict the **FWI (Fire Weather Index)**, which helps assess fire risk based on weather and fuel conditions.

The project covers:

- Data Analysis & Feature Engineering
- Model Training & Evaluation
- Model Serialization
- Web Deployment using Flask

---

## 📂 Project Structure

```
projectendtoend/
│
├── application.py                # Flask application
├── models/
│   ├── ridge.pkl                 # Trained Ridge Regression model
│   └── scaler.pkl                # StandardScaler used during training
│
├── notebooks/
│   ├── 2.0-EDA And FE Algerian Forest Fires.ipynb
│   └── 3.0-Model Training.ipynb
│
├── templates/
│   ├── index.html                # Landing page
│   └── home.html                 # Prediction form & result page
│
├── Algerian_forest_fires_dataset_UPDATE.csv
├── requirements.txt
└── README.md
```

---

## 📊 Dataset Information

- **Dataset**: Algerian Forest Fires Dataset

- **Source**: UCI Machine Learning Repository

- **Features Used**:
  - Temperature
  - Relative Humidity (RH)
  - Wind Speed (Ws)
  - Rain
  - FFMC
  - DMC
  - ISI
  - Classes
  - Region

- **Target Variable**:
  - Fire Weather Index (FWI)

---

## 🧠 Model Details

- **Algorithm**: Ridge Regression
- **Preprocessing**:
  - Feature scaling using `StandardScaler`

- **Reason for Ridge**:
  - Handles multicollinearity
  - Prevents overfitting
  - Performs well on continuous prediction tasks

---

## 🌐 Flask Web Application

The Flask app provides:

- A homepage (`/`)
- A prediction page (`/predictdata`) where users enter input features
- Real-time FWI prediction displayed on the web page

### 🔗 Routes

| Route          | Description             |
| -------------- | ----------------------- |
| `/`            | Landing page            |
| `/predictdata` | Input form & prediction |

---

## ▶️ How to Run the Project Locally

### 1️⃣ Clone the repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd projectendtoend
```

### 2️⃣ Create & activate environment (recommended)

```bash
conda create -n fwi python=3.10 -y
conda activate fwi
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Flask app

```bash
python application.py
```

### 5️⃣ Open in browser

```
http://127.0.0.1:5001
```

---

## ⚠️ Important Notes

- The project uses **scikit-learn model persistence** (`pickle`).
- Ensure the **same sklearn version** is used for training and inference to avoid warnings.
- Flask is run on **port 5001** to avoid macOS port conflicts.

---

## 🚀 Future Improvements

- Add logging & exception handling
- Improve UI with CSS/Bootstrap
- Add Docker support
- Deploy on cloud platforms (Render / Railway / AWS)
- Use CI/CD for automated deployment

---

## 👨‍💻 Author

**Madhav Manoj**
B.Tech CSE
Machine Learning & AI Enthusiast

---

⭐ If you find this project useful, don’t forget to **star the repository**!
