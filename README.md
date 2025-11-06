# Loan Approval Prediction - Flask App

A simple Flask web app to predict loan approval using a trained pipeline (`loan_pipeline.pkl`).

## Prerequisites
- Python 3.10+ recommended
- Windows Command Prompt or PowerShell

## Setup
1. Create & activate a virtual environment (recommended):

```bat
python -m venv .venv
".venv\\Scripts\\activate"
```

2. Install dependencies:

```bat
pip install --upgrade pip
pip install -r requirements.txt
```

## Run the app (local)
Either:
```bat
python app.py
```

Or using Flask CLI:
```bat
set FLASK_APP=app.py
set FLASK_ENV=development
flask run
```

Then open `http://127.0.0.1:5000/` in your browser.

## Files
- `app.py`: Flask server loading `loan_pipeline.pkl` and serving the form
- `templates/index.html`: HTML form and result display
- `static/style.css`: Styling
- `loan_pipeline.pkl`: Trained preprocessing+model pipeline (required)

## Notes
- Ensure `loan_pipeline.pkl` is present next to `app.py`.
- Input field names match training features; the pipeline handles preprocessing and encodings.
- For production (Linux), you can use Gunicorn: `gunicorn -w 2 -b 0.0.0.0:5000 app:app`.

