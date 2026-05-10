# AutoML Training and Optimization System

A lightweight, offline desktop AutoML application that takes a CSV dataset and a plain-English description of your goal, then automatically builds, compares, and optimizes machine learning pipelines — no manual coding required.

Built with Python as an AI course project at Bahria University.

---

## What it does

1. **Upload a CSV** — the app validates and loads your tabular dataset
2. **Describe your goal in plain English** — NLP (spaCy) detects whether it's a classification or regression task and identifies the target column automatically
3. **Pipeline runs automatically** — preprocessing, feature engineering, baseline model comparison, and hyperparameter tuning all happen without user intervention
4. **Get a full report** — results, plots, and a downloadable ZIP are generated at the end

---

## Features

- NLP-driven task detection (classification vs regression) using spaCy
- Automatic or manual target column selection
- Modular ML pipelines for both task types
- Baseline comparison across multiple models before optimization
- Hyperparameter tuning via Optuna (balanced for speed and accuracy)
- Visualizations: feature importance, correlation heatmaps, confusion matrices, residual plots
- Exportable reports in TXT + HTML + ZIP format
- Real-time execution logs in the GUI
- Fully offline — no cloud, no subscription

---

## Models

| Task | Models |
|------|--------|
| Regression | Linear Regression, Random Forest Regressor, XGBoost Regressor |
| Classification | KNN, Random Forest Classifier, Neural Network |

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Language | Python 3.x |
| ML | scikit-learn, XGBoost |
| NLP | spaCy |
| Hyperparameter Tuning | Optuna |
| Visualization | Matplotlib, Seaborn |
| GUI | Tkinter |
| IDE | VS Code |

---

## Datasets Tested On

| Dataset | Size | Task |
|---------|------|------|
| California Housing | 20,641 rows | Regression |
| Bank Marketing | 41,000 rows | Classification |
| Hotel Booking | 119,000 rows | Classification |
| Loan Approval | 50,000 rows | Classification |
| Anime List Ratings | 20,000 rows | Regression |

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/automl-training-system.git
cd automl-training-system

# Install dependencies
pip install -r requirements.txt
python -m spacy download en_core_web_sm

# Run the app
python main.py
```

---

## Project Structure

```
automl-training-system/
├── main.py                  # Entry point, launches GUI
├── backend/
│   ├── core.py              # Coordinates pipeline execution
│   ├── nlp_detector.py      # spaCy-based task & target detection
│   ├── regression_pipeline.py
│   ├── classification_pipeline.py
│   ├── plotting.py          # All visualizations
│   └── report_generator.py  # TXT/HTML/ZIP report output
├── gui/
│   └── app.py               # Tkinter interface
├── requirements.txt
└── README.md
```

---
<img width="659" height="421" alt="image" src="https://github.com/user-attachments/assets/10a028a3-457a-48ad-984c-5a15373a7262" />
<img width="663" height="250" alt="image" src="https://github.com/user-attachments/assets/e33c8cd2-9f2c-4221-a0b6-4e914c79b905" />
