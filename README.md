
# 🌾 Smart Sprinkler Controller using AI for Irrigation Management

An AI-powered **Smart Sprinkler Controller** that predicts the ON/OFF status of 20 sprinklers (parcel_0 to parcel_19) based on real-time sensor input, developed as part of **AICTE Virtual Internship 2025 – Cycle 2 (S4F)**.

---

## 📌 Table of Contents
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Proposed Solution](#proposed-solution)
- [Architecture](#architecture)
- [Tech Stack Used](#tech-stack-used)
- [Installation Steps](#installation-steps)
- [How to Run](#how-to-run)
- [Model Overview](#model-overview)
- [Features](#features)
- [Sample Use-Case](#sample-use-case)
- [Output Screenshot](#output-screenshot)
- [Future Scope](#future-scope)
- [Acknowledgements](#acknowledgements)
- [File Structure](#file-structure)

---

## 📖 Problem Statement

Traditional irrigation systems often result in excessive water usage due to lack of automation and real-time data analysis. Inconsistent irrigation reduces crop yield and wastes valuable resources.

---

## 🎯 Objectives

- Automate sprinkler control using AI.
- Utilize real-time sensor data to make intelligent irrigation decisions.
- Deploy a user-friendly application that accepts scaled sensor inputs and displays the status of each sprinkler.

---

## 💡 Proposed Solution

Developed a machine learning model using a **Random Forest Classifier** trained on real-world sensor data. The model predicts ON/OFF states for **20 sprinkler zones** based on sensor readings. A **Streamlit app** provides a simple interface for users to interact with the system.

---

## 🧩 Architecture

1. User Inputs 20 scaled sensor values (between 0 and 1) using sliders in the Streamlit UI
2. Streamlit Backend collects input and converts it into a NumPy array
3. Machine Learning Model (Random Forest) predicts ON/OFF states for each of the 20 sprinklers
4. Results Displayed dynamically in the web interface showing which parcels need irrigation

---

## 🛠 Tech Stack Used

- **Python**
- **Pandas**, **NumPy**, **Scikit-learn**
- **Streamlit**
- **Joblib** (for model serialization)
- **Matplotlib & Seaborn** (for visualization during training)

---

## ⚙️ Installation Steps

1. Clone the repository:

```bash
git clone https://github.com/your-username/smart-irrigation-system.git
cd smart-irrigation-system
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Ensure the trained model file is present:

- `Farm_Irrigation_System.pkl` – machine learning model (included)

---

## ▶️ How to Run

Run the Streamlit app:

```bash
streamlit run app.py
```

Then open the local URL in your browser to interact with the Smart Irrigation interface.

---


## 🧠 Model Overview

- **Model Used**: `RandomForestClassifier` wrapped with `MultiOutputClassifier`
- **Preprocessing**: Scaled input features using `MinMaxScaler`
- **Trained On**: Dataset with 20 input features and 20 output sprinkler labels
- **Evaluation**: Used `classification_report` for performance metrics

---

## ✨ Features

- Takes **20 scaled sensor inputs (0 to 1)** using sliders
- Predicts **ON/OFF status of each sprinkler (parcel_0 to parcel_19)**
- Fully functional local app using **Streamlit**
- Easy to use interface with clean layout

---

## 💼 Sample Use-Case

A farmer can input current sensor values (like temperature, moisture, etc. scaled to 0–1) into the app. The model will predict which sprinkler zones should be turned ON to optimize water usage and crop health.

---

## 📸 Output Screenshot

- **Input Interface**

<img width="748" height="750" alt="image" src="https://github.com/user-attachments/assets/f2d7090b-3244-4e66-987b-4d3966ac6b1e" />

<img width="765" height="778" alt="image" src="https://github.com/user-attachments/assets/43da7d64-1fc5-4a9c-acac-793b06507964" />

<img width="752" height="668" alt="image" src="https://github.com/user-attachments/assets/a00e86c7-3a88-4539-bb83-46575d0cade7" />

- **Prediction Output**

<img width="320" height="311" alt="image" src="https://github.com/user-attachments/assets/2ab32805-15d3-48be-997a-08c268d1bbc8" />

## 🚀 Future Scope

- Integrate real-time IoT sensor data
- Deploy the model on embedded systems for offline use
- Include weather API for rain prediction
- Add mobile-responsive UI and notifications

---

## 🙏 Acknowledgements

- **Edunet Foundation**
- **AICTE**
- **Shell India**
- **Mentor**: Hariharan Sir  
- **Coordinator**: Nikita Ma’am – [LinkedIn](https://www.linkedin.com/in/nikita)

---

## 📁 File Structure

```
smart-irrigation-system/
│
├── app.py                         # Streamlit App
├── Farm_Irrigation_System.pkl     # Trained ML Model
├── irrigation_machine.csv         # Dataset (optional)
├── week 3 task.ipynb              # Notebook with training & preprocessing
├── requirements.txt               # Python dependencies
└── README.md                      # Documentation
```

---
