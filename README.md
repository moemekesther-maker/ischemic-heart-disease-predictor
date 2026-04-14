# Ischemic-heart-disease-predictor

An end-to-end machine learning project that predicts the risk of Ischemic Heart Disease
(IHD) from clinical features, with a deployed interactive web application.
 Datasets Used
Dataset
Rows
Purpose
hypertension_data.csv
26,083
Cleveland Heart Disease dataset — provides IHD
labels
diabetes_data.csv
70,692
Lifestyle and metabolic risk factors
stroke_data.csv
40,910
Comorbidity features (glucose, BMI, smoking)
 Project Structure
ihd_project/
├── data/
│   
├── hypertension_data.csv
│   
│   
│
├── diabetes_data.csv
└── stroke_data.csv
├── phase1_understand_data.py       
├── phase2_eda.py                   
← Data dictionary, column inspection, target analysis
← 8 exploratory plots
├── phase3_feature_engineering.py  ← Feature engineering, encoding, dataset prep
├── phase4_model_building.py       
← Train 5 models + hyperparameter tuning
├── phase5_evaluation.py           
├── phase6_streamlit_app.py        
│
├── outputs/
│   
├── eda/                        
│   
│   
│   
├── processed/                  
├── models/                     
└── evaluation/                 
← ROC curves, SHAP values, confusion matrix
← Interactive web app for deployment
← EDA plots
← Cleaned feature CSV
← Saved model .pkl files
← Evaluation plots + report
│
├── requirements.txt
└── README.md
 How to Run
1. Install dependencies
pip install -r requirements.txt
2. Add data files
Place all three CSV files in a data/ folder.
3. Run phases in order
python phase1_understand_data.py
python phase2_eda.py
python phase3_feature_engineering.py
python phase4_model_building.py
python phase5_evaluation.py
4. Launch the app
streamlit run phase6_streamlit_app.py
 Model Performance
Model
Accuracy
Recall
XGBoost
—
F1
AUROC
—
Random Forest
—
—
—
—
Gradient Boosting
—
—
—
—
Logistic Regression
—
—
—
—
MLP Neural Network
—
—
—
—
—
—
(Fill in after running Phase 4)
 Key Engineered Features
hr_reserve — difference between age-predicted max HR and actual max HR
metabolic_risk_score — composite of normalised BP + cholesterol
angina_st_combo — exercise angina AND ST depression co-occurrence
vessel_thal_risk — blocked vessels × reversable thalassemia interaction
age_sex_risk — age threshold adjusted for sex (male ≥45, female ≥55)
 Live Demo
[Add your Streamlit Cloud URL here after deployment]
⚠ Disclaimer
This project is for educational and portfolio purposes only. It does not constitute
medical advice and must not be used for clinical decisions.
 References
Detrano, R. et al. (1989). International application of a new probability algorithm for
the diagnosis of coronary artery disease. American Journal of Cardiology.
UCI Machine Learning Repository — Cleveland Heart Disease Dataset
