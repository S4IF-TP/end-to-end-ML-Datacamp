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

Quick start

1. Create a virtual environment and activate it (recommended):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install -r requirements.txt
```

3. Open the notebooks with Jupyter:

```powershell
python -m notebook
```

Contributing

- Add a folder per course module or exercise category when needed.
- Keep notebooks focused: one exercise per notebook when possible.
- Use the template notebook for consistent headers and metadata.

License

This project is licensed under the MIT License — see the `LICENSE` file for details.

Notebook conventions

- File names: prefix notebooks with a two-digit index and short slug, e.g. `01-iris-exercise.ipynb`.
- Keep one exercise per notebook when possible. Use the template `00-template.ipynb` for headers and standard imports.
- Keep large datasets out of Git; place small reproducible CSVs under `data/` and add them to the repo if necessary.
- Add a short README inside subfolders if the folder contains multiple notebooks.

Recommended workflow

1. Create a branch for each module or set of exercises: `git checkout -b module-1-exercises`.
2. Commit notebooks and small data files. For big data, store a download script or provide a note in the notebook describing how to obtain it.
3. Use clear cell titles and markdown to explain your approach and results.

Further improvements (optional)

- Add automated checks (pre-commit hooks) to clear outputs before committing large notebooks.
- Add unit tests for any reusable helper functions placed in a `src/` folder.

If you'd like, I can also:

- Add pre-commit configuration to strip notebook outputs automatically.
- Add a simple `src/` module and accompanying tests for notebook helper utilities.

## MLflow experiments (optional)

This repo includes an MLflow module (`05-mlflow-experiments.ipynb`) to track experiment runs.

Run the UI to compare runs (after installing requirements):

```powershell
mlflow ui
```

Notes

- By default, MLflow stores runs under a local `mlruns/` folder (ignored in git).
- You can change the tracking URI via:

```powershell
$env:MLFLOW_TRACKING_URI = "file:./mlruns"
```

See the notebook for examples of: `set_experiment`, `start_run`, `log_param`, `log_metric`, `get_run`, and `search_runs`.
