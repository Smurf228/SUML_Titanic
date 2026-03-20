# SUML Titanic — Survival Prediction (Streamlit + scikit-learn)

A small **Streamlit** web app that predicts whether a passenger would survive the **Titanic** disaster using a pre-trained **scikit-learn** model.

The model was trained on the classic Kaggle dataset: *Titanic: Machine Learning from Disaster*.

## Features

- Interactive UI (Streamlit) to input passenger features
- `model.sv` — serialized scikit-learn model (loaded via `pickle`)
- Predicts **Survived / Not Survived** and shows prediction probability

## Tech stack

- Python
- Streamlit
- scikit-learn

## Repository contents

- `zad4.py` — Streamlit application entry point
- `requirements.txt` — minimal dependencies
- `model.sv` — trained model file (pickle)

## Getting started

### 1) Create and activate a virtual environment (recommended)

**macOS/Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows (PowerShell)**

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 2) Install dependencies

```bash
pip install -r requirements.txt
```

### 3) Run the Streamlit app

```bash
streamlit run zad4.py
```

Then open the local URL printed in the terminal (usually `http://localhost:8501`).

## Model inputs

The app asks for the following passenger attributes (in the same order used by the model):

- `Pclass` (ticket class)
- `Sex`
- `Age`
- `SibSp` (siblings/spouses aboard)
- `Parch` (parents/children aboard)
- `Fare`
- `Embarked` (port of embarkation)

## Notes / limitations

- `model.sv` must be present in the project root next to `zad4.py`.
- The UI text in the app is currently in Polish.
- The code contains a small compatibility workaround for loading pickled models across OS path implementations.

## License

No license file is included in this repository. If you plan to reuse this code, consider adding a license.