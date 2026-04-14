# Ischemic-heart-disease-predictor

An end-to-end machine learning project that predicts the risk of **Ischemic Heart Disease (IHD)** using clinical, metabolic, and lifestyle features. The project includes data processing, model training, evaluation, and deployment via an interactive **Streamlit web application**.

---

## 📊 Datasets Used

| Dataset                 | Rows   | Purpose                                               |
| ----------------------- | ------ | ----------------------------------------------------- |
| `hypertension_data.csv` | 26,083 | Cleveland Heart Disease dataset — provides IHD labels |
| `diabetes_data.csv`     | 70,692 | Lifestyle and metabolic risk factors                  |
| `stroke_data.csv`       | 40,910 | Comorbidity features (glucose, BMI, smoking, etc.)    |

---

## 📁 Project Structure

```
ihd_project/
├── data/
│   ├── hypertension_data.csv
│   ├── diabetes_data.csv
│   └── stroke_data.csv
│
├── phase1_understand_data.py        # Data dictionary, column inspection, target analysis
├── phase2_eda.py                   # Exploratory Data Analysis (8 plots)
├── phase3_feature_engineering.py   # Feature engineering and dataset preparation
├── phase4_model_building.py        # Train 5 models + hyperparameter tuning
├── phase5_evaluation.py            # Evaluation metrics and visualizations
├── phase6_streamlit_app.py         # Interactive web app (Streamlit)
│
├── outputs/
│   ├── eda/                        # EDA plots
│   ├── processed/                  # Cleaned feature dataset
│   ├── models/                     # Saved model (.pkl files)
│   └── evaluation/                 # ROC curves, SHAP values, confusion matrix
│
├── requirements.txt
└── README.md
```

---

## ⚙️ How to Run

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Add Data Files

Place all three CSV files in the `data/` folder.

### 3. Run Project Phases (in order)

```bash
python phase1_understand_data.py
python phase2_eda.py
python phase3_feature_engineering.py
python phase4_model_building.py
python phase5_evaluation.py
```

### 4. Launch the Web App

```bash
streamlit run phase6_streamlit_app.py
```

---

## 🤖 Models Used

* XGBoost
* Random Forest
* Gradient Boosting
* Logistic Regression
* MLP Neural Network

---

## 📈 Model Performance

| Model               | Accuracy | Recall | F1 Score | AUROC |
| ------------------- | -------- | ------ | -------- | ----- |
| XGBoost             | —        | —      | —        | —     |
| Random Forest       | —        | —      | —        | —     |
| Gradient Boosting   | —        | —      | —        | —     |
| Logistic Regression | —        | —      | —        | —     |
| MLP Neural Network  | —        | —      | —        | —     |

*(Fill in after running Phase 4 & 5)*

---

## 🧠 Key Engineered Features

* **hr_reserve** — Difference between age-predicted max heart rate and actual max HR
* **metabolic_risk_score** — Composite of normalized blood pressure + cholesterol
* **angina_st_combo** — Interaction of exercise-induced angina and ST depression
* **vessel_thal_risk** — Blocked vessels × reversible thalassemia interaction
* **age_sex_risk** — Age threshold adjusted by sex (male ≥45, female ≥55)

---

## 🌐 Live Demo

[Add your Streamlit Cloud URL here after deployment]

---

## ⚠️ Disclaimer

This project is for **educational and portfolio purposes only**.
It is **not medical advice** and must not be used for real clinical decision-making.

---

## 📚 References

* Detrano, R. et al. (1989). *International application of a new probability algorithm for the diagnosis of coronary artery disease*. American Journal of Cardiology.
* UCI Machine Learning Repository — Cleveland Heart Disease Dataset

---

## 🚀 Future Improvements

* Add cross-validation and model ensembling
* Improve feature selection using SHAP importance
* Deploy with Docker for production use
* Integrate real-time health data inputs

---

## 👨‍💻 Author

Esther Moemeke
https://github.com/moemekesther-maker

---

