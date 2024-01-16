## See the [Frontend](https://github.com/PH-Tools/PH_View_React)

## Installation / Setup for local development
1) `python3 -m venv .venv`
1) `source .venv/bin/activate`
1) `pip install -r requirements.txt`


## Run Locally in development-mode
1) `source .venv/bin/activate`
1) Make sure `origins = ["http://localhost:3000", ...]` is set in `main.py` to support React
1) Run `uvicorn main:app --reload`

## Deployment to [Render.com](https://render.com/)
1) Make sure `origins = [..., "https://bldgtyp.github.io"]` is set in `main.py` to fix CORS 
1) Push to GitHub
1) Render | Settings | `Start command`: `uvicorn main:app --host 0.0.0.0 --port $PORT`
1) Manually Deployment
1) View it on [https://ph-view.onrender.com/](https://ph-view.onrender.com/)