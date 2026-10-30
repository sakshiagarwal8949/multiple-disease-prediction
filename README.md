# 🏥 Multiple Disease Prediction System using Machine Learning & Streamlit

A web application built using **Streamlit** and **Machine Learning (Scikit-Learn)** that predicts whether a patient has a particular disease based on clinical input parameters.

---

## 📋 Features & Supported Predictions

1. **Diabetes Prediction**: Predicts diabetes risk using medical metrics (Glucose, Blood Pressure, Insulin, BMI, Age, etc.).
2. **Heart Disease Prediction**: Predicts presence of heart disease based on cardiovascular parameters (Cholesterol, Resting BP, Max Heart Rate, etc.).
3. **Parkinson's Disease Prediction**: Predicts Parkinson's disease using various voice and frequency biomedical measurements.

---

## 🗂️ Project Directory Structure

```text
multiple-disease-prediction-streamlit-app/
│
├── app.py                           # Main Streamlit web application
├── requirements.txt                 # Python dependencies
├── README.md                        # Documentation and execution steps
│
├── saved_models/                    # Pre-trained ML model files (.sav)
│   ├── diabetes_model.sav
│   ├── heart_disease_model.sav
│   └── parkinsons_model.sav
│
├── dataset/                         # Datasets used for training
│   ├── diabetes.csv
│   ├── heart.csv
│   └── parkinsons.csv
│
└── colab_files_to_train_models/     # Jupyter/Colab notebooks for model training
    ├── Multiple disease prediction system - diabetes.ipynb
    ├── Multiple disease prediction system - heart.ipynb
    └── Multiple disease prediction system - Parkinsons.ipynb
```

---

## ⚙️ Prerequisites

- **Python**: Version `3.9`, `3.10`, or `3.11` recommended.
- **pip**: Python package installer (comes bundled with Python).

---

## 🚀 Step-by-Step Guide: How to Run in Terminal

Follow these terminal steps one by one to set up and run the application:

### Step 1: Open Terminal & Navigate to Project Directory

Open **Command Prompt**, **PowerShell**, or **Git Bash**, and navigate to this folder:

```bash
cd path/to/multiple-disease-prediction-streamlit-app-main
```
*(Replace `path/to/...` with your actual folder path where this project is located)*

---

### Step 2: (Recommended) Create & Activate a Virtual Environment

Creating an isolated virtual environment prevents library version conflicts:

- **On Windows (PowerShell / Command Prompt):**
  ```bash
  python -m venv venv
  .\venv\Scripts\activate
  ```

  > **Note for Windows PowerShell users:** If you see an error like `cannot be loaded because running scripts is disabled on this system`, run this command first and retry:
  > ```powershell
  > Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
  > .\venv\Scripts\activate
  > ```

- **On macOS / Linux:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

---

### Step 3: Install Required Libraries

Install all necessary packages using `requirements.txt`:

```bash
pip install -r requirements.txt
```

*(Packages installed: `numpy`, `scikit-learn`, `streamlit`, `streamlit-option-menu`)*

---

### Step 4: Run the Streamlit Application

Execute the following command in your terminal:

```bash
streamlit run app.py
```

> **Alternative command** (if `streamlit` is not recognized directly in your terminal):
> ```bash
> python -m streamlit run app.py
> ```

---

### Step 5: Access the Web App

Once the command is executed, Streamlit will display local and network URLs in the terminal:

```text
  You can now view your Streamlit app in your browser.

  Local URL: http://localhost:8501
  Network URL: http://192.168.x.x:8501
```

If it does not open automatically, open your browser and visit:
👉 **[http://localhost:8501](http://localhost:8501)**

---

## 🛑 How to Stop the App

To stop the Streamlit server, go back to your terminal and press:
- **`Ctrl + C`**

To deactivate the virtual environment (when finished):
```bash
deactivate
```

---

## ⚠️ Important Usage Notes & Troubleshooting

1. **Fill All Input Fields**:
   Make sure to enter valid numerical values into **all input boxes** before clicking the prediction button. Empty or non-numeric values will cause a `ValueError`.
2. **Scikit-Learn Version Compatibility**:
   The pre-trained models (`.sav` files) were serialized with `scikit-learn==1.3.2`. If you encounter unpickling errors, ensure `scikit-learn==1.3.2` is installed:
   ```bash
   pip install scikit-learn==1.3.2
   ```
3. **Retraining the Models**:
   If you wish to re-train the models or use updated data, open and execute the notebooks inside `colab_files_to_train_models/` using Google Colab or Jupyter Notebook, then save the generated `.sav` files into the `saved_models/` directory.

---

## 📄 License & Attribution
Created for educational and research purposes. Medical decisions should always be consulted with certified medical professionals.
