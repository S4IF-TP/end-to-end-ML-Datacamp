# End-to-End ML — Datacamp Course Exercises

This repository collects exercises, notes, and reproducible notebooks for the "End to End ML" course on Datacamp.

## Case Study: CardioCare Heart Disease Prediction

This course follows a real-world case study where we build a machine learning model for **CardioCare clinic** to predict the risk of heart disease in patients. The model will:

- Provide binary predictions (heart disease: yes/no) to inform cardiologist decision-making
- Match or exceed human expert performance
- Be reliable, secure, interpretable, and continuously monitored
- Handle sensitive patient data (age, cholesterol, blood pressure, etc.) with privacy and security

**Important**: The model informs decisions, it does not make them—especially critical in healthcare.

## The Machine Learning Lifecycle

This course follows the typical ML lifecycle:

1. **Problem Understanding & Definition** — align with stakeholders (CardioCare), set clear objectives
2. **Data Collection & Preparation** — gather patient health data, understand context and potential biases
3. **Model Development & Tuning** — build and optimize the prediction model
4. **Model Evaluation** — validate performance and generalization
5. **Deployment** — make the model available for real-time predictions
6. **Monitoring** — continuously track performance and retrain when needed

The process is iterative—we cycle through stages as the project and data evolve.

Repository structure

- `README.md` — this file
- `notebooks/` — Jupyter notebooks for exercises and templates
  - `00-template.ipynb` — Notebook template and instructions
  - `01-problem-understanding.ipynb` — Module 1: Problem definition, business requirements, data collection
  - `02-data-preparation.ipynb` — Module 2: Data cleaning and preprocessing (upcoming)
  - More modules to be added as course progresses...
- `data/` — (optional) patient health datasets used in exercises; kept out of git when large or sensitive
- `.gitignore` — recommended ignores
- `LICENSE` — MIT license
- `requirements.txt` — minimal dependencies for the notebooks

