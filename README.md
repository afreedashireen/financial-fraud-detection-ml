# Financial Fraud Detection using Machine Learning, NLP & Explainable AI

An MSc Data Science & Analytics research project investigating financial fraud detection using machine learning, natural language processing, explainable AI and data visualisation.

The project combines **structured insurance claims analysis** with **unstructured financial complaint analysis** to explore both supervised fraud classification and fraud-risk estimation from unlabelled text.

## 🎯 Project Objectives

* Develop machine learning models for fraud detection on structured insurance claims data.
* Investigate the effect of class imbalance and data leakage on model performance.
* Apply explainable AI techniques to understand the features driving fraud predictions.
* Analyse unlabelled financial complaint text using NLP and weak supervision.
* Improve the reliability of weak fraud-risk labels through consistency and quality filtering.
* Present analytical findings through interpretable visualisations and dashboards.

## 📊 Data Sources

### Structured Insurance Claims Data

The structured component uses automobile insurance claims data containing policy, claimant, accident and claim-related attributes.

This dataset is used for supervised fraud classification, feature selection, model comparison and explainability analysis.

### CFPB Consumer Complaint Data

The NLP component uses consumer financial complaint narratives from the Consumer Financial Protection Bureau (CFPB).

Because confirmed fraud labels are not available for these complaint narratives, the project treats this component as **fraud-risk estimation rather than confirmed fraud classification**.

## 🔬 Methodology

The project includes:

* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Feature engineering
* Class imbalance analysis
* SMOTE experimentation
* Leakage-aware model evaluation
* Binary Particle Swarm Optimisation (BPSO) for feature selection
* Comparison of multiple machine learning classifiers
* SHAP-based model explainability
* NLP analysis of financial complaint narratives
* BART-MNLI based weak supervision
* Coherence filtering
* Weak-label quality assessment
* CleanLab-based validation
* Fraud-risk evidence integration
* Analytical visualisation and dashboard preparation

## ⚠️ Data Leakage Experiment

An important part of this research examines the effect of applying **SMOTE before the train-test split**.

This approach can allow synthetic information derived from the overall dataset to influence both training and testing data, producing overly optimistic evaluation results.

The project therefore contrasts these results with a **leakage-aware workflow**, where resampling is restricted to the training data.

This comparison demonstrates why high model accuracy alone is not sufficient evidence of reliable fraud detection performance.

## 🔍 Explainable AI with SHAP

SHAP is used to move beyond simply predicting whether a claim is potentially fraudulent.

The analysis examines **which features contribute most strongly to individual and overall fraud predictions**, improving model transparency and making the results easier to interpret for business stakeholders.

## 📝 NLP & Weak Supervision

The CFPB complaint dataset does not contain confirmed fraud labels.

Instead of treating generated labels as ground truth, the project uses **BART-MNLI based weak supervision** to estimate fraud-related signals from complaint narratives.

Additional filtering and validation techniques are used to identify inconsistent or unreliable weak labels.

The resulting outputs should therefore be interpreted as **fraud-risk estimates**, not confirmed fraud classifications.

## 🛠️ Technologies

**Programming & Analysis**

* Python
* Pandas
* NumPy
* Scikit-learn

**Machine Learning & Explainability**

* Classification models
* SMOTE
* Binary Particle Swarm Optimisation
* SHAP
* CleanLab

**Natural Language Processing**

* BART-MNLI
* Weak Supervision
* Text Processing
* Coherence Filtering

**Visualisation**

* Matplotlib
* Power BI

## 📁 Repository Structure

```text
financial-fraud-detection-ml/
│
├── notebooks/
│   ├── README.md
│   └── financial_fraud_detection_complete_pipeline.ipynb
│
├── images/
│
├── .gitignore
│
└── README.md
```

## 📓 Notebook

The complete research implementation is available in:

`notebooks/financial_fraud_detection_complete_pipeline.ipynb`

The notebook contains the end-to-end analytical workflow covering preprocessing, exploratory analysis, machine learning, feature selection, explainability, NLP weak supervision and evaluation.

## 💡 Key Research Insight

One of the central findings of this project is that **evaluation methodology can substantially affect apparent fraud-detection performance**.

The research highlights the importance of preventing data leakage, interpreting weak supervision carefully and combining predictive performance with explainability when developing fraud analytics systems.

## 🚀 Future Work

Future development could investigate transformer-based models such as **BERT** using carefully filtered weak-supervision labels, with additional validation mechanisms to reduce label noise and improve confidence in fraud-risk estimation.

---

### Author

**Afreeda Shireen**
MSc Data Science & Analytics,
Data Analytics | SQL | Power BI | Python | Machine Learning | Insurance Analytics
