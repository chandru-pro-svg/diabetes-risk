# 🩺 Diabetes Risk Estimator

An interactive machine-learning web application that estimates diabetes risk using a trained **Logistic Regression** model based on 8 standard clinical and physiological indicators. The tool calculates real-time risk probabilities against a 50% decision threshold and provides transparent odds ratios to highlight which inputs drive the prediction.

---

## 🌐 Live Demo

👉https://diabetes-risk-estimator.vercel.app/


---

## 📌 Project Overview

This tool applies machine learning to diabetes risk screening, allowing users to enter diagnostic values or test sample cases to view immediate statistical predictions.

Key capabilities:

* **Instant Risk Probability:** Computes real-time percentage risk through a dynamic semi-circular gauge.


* **Threshold Stratification:** Compares current estimates against a 50% clinical decision threshold (e.g., *Lower estimated risk* vs *Higher estimated risk*).


* **Explainable Odds Analysis:** Itemizes feature-level impact on odds compared to an average patient baseline (showing multipliers such as odds × 1.00, odds × 0.71, etc.).


* **Quick-Load Presets:** Pre-fills inputs using one-click profiles (**Load typical profile** / **Load higher-risk profile**) for rapid testing.



---

## ⚙️ Input Parameters (8 Clinical Inputs)

The predictive model evaluates eight standard physiological and medical history factors:

| Category | Input Feature | Measurement / Unit | Description |
| --- | --- | --- | --- |
| **Clinical Measurements** | **Glucose** | mg/dL | Plasma glucose concentration (2 hours post-glucose drink)

 |
|  | **Blood Pressure** | mm Hg | Diastolic blood pressure

 |
|  | **Insulin** | µU/mL | 2-hour serum insulin

 |
|  | **Skin Thickness** | mm | Triceps skinfold thickness

 |
| **Body & History** | **BMI** | kg/m² | Body Mass Index

 |
|  | **Family History Score** | Index | Diabetes Pedigree Function

 |
|  | **Age** | Years | Patient age

 |
|  | **Pregnancies** | Count | Number of times pregnant

 |

---

## 🛠️ Tech Stack & Architecture

* **Machine Learning:** Python, Scikit-Learn (Logistic Regression model)
* **Model File:** Serialized Pickle file (`logistmodel.pkl`)[cite: 5]
* **Frontend / Client Logic:** HTML5, CSS3, Modern JavaScript with real-time slider controls and SVG gauges[cite: 4, 5]
* **Deployment Platform:** [Vercel](https://vercel.com)[cite: 4, 5]

---

## 📂 Repository Structure

```text
├── Diabetes risk estimator.html   # Main application interface and client scripts
├── logistmodel.pkl                # Serialized trained Logistic Regression model
└── README.md                      # Project documentation

```

*(Files in repository[cite: 5])*

---

## 🚀 Getting Started Locally

To run the application locally on your machine:

1. **Clone the repository:**
```bash
git clone https://github.com/chandru-pro-svg/diabetes-risk.git
cd diabetes-risk

```


2. **Launch the interface:**
* Open `Diabetes risk estimator.html` directly in any web browser, or serve it with Python[cite: 5]:
```bash
python -m http.server 8000

```


* Access `http://localhost:8000/Diabetes%20risk%20estimator.html` in your browser[cite: 5].



---

## 🔍 How It Works

1. The user inputs patient metrics using interactive sliders and numerical fields, or selects a sample profile preset.


2. The client formats and maps the 8 clinical inputs against the model coefficients.
3. The saved model (`logistmodel.pkl`) computes the logistic sigmoid risk probability score[cite: 4, 5].
4. The web application dynamically renders the risk percentage, updates the gauge, and details the individual log-odds drivers.



---

## 📈 Future Improvements

* Integrate additional algorithms (e.g., Random Forest, XGBoost) for side-by-side performance benchmarking.
* Enable PDF report generation and download for clinical summaries.
* Add SHAP/LIME-based explainability visual plots for deeper interpretability.
* Provide responsive multi-language localization.

---

## ⚠️ Disclaimer

> **Educational & Screening Aid Only:** This web application is driven by a statistical machine learning model trained on historical data. It does not constitute medical advice, a diagnosis, or a treatment plan. Always consult a qualified healthcare professional for medical assessments.

---

## 👤 Author

**Chandru** GitHub: [@chandru-pro-svg](https://www.google.com/search?q=https://github.com/chandru-pro-svg)[cite: 5, 6]

⭐ **If you like this project, give it a star!**[cite: 6]
