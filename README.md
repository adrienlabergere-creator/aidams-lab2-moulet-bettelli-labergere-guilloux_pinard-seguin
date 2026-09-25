# AIDAMS Lab 2

This project contains our Lab 2 notebook on the modelling lifecycle, using the Global Iron and Steel Tracker (GIST) plant-level data.

## Project structure

```text
.
├── lab_2.ipynb
├── data/
│   ├── Plant-level_data_Global_Iron_and_Steel_Tracker_June_2026_V1.xlsx
│   └── other downloaded GIST files
└── README.md
```

The notebook uses operating crude steel capacity as a transparent proxy for production because the GIST release does not provide one comparable observed-production variable for every plant.

## Setup on Windows

Open PowerShell in the project folder and create a virtual environment:

```powershell
py -m venv .venv
```

Activate it:

```powershell
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, run this once for the current terminal:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Install the required packages:

```powershell
python -m pip install --upgrade pip
python -m pip install pandas numpy matplotlib seaborn scikit-learn pandera mlflow optuna optuna-integration[mlflow] joblib openpyxl jupyter
```

## Run the notebook

```powershell
jupyter notebook lab_2.ipynb
```

Alternatively, open the notebook in VS Code and select the Python interpreter from `.venv`. Run the cells from top to bottom.

The notebook creates `best_steel_pipeline.joblib`, `feature_list.json`, and a local `mlflow.db` file when the lifecycle cells are run.
