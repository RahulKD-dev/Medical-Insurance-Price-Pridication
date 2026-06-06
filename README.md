# Medical Insurance Price Prediction

A full-stack web application that predicts medical insurance costs using a machine learning model, allows users to compare insurance companies, and purchase plans.

## Features

- **Price Prediction** — Predicts insurance charges based on age, BMI, smoking status, region, gender, and number of children
- **Company Listing** — Browse and compare available insurance companies
- **Purchase Flow** — Buy insurance plans with multiple payment methods
- **User Dashboard** — View purchase history
- **Admin Panel** — Manage insurance companies
- **Authentication** — Register and login with role-based access (user / admin)
- **Documentation** — In-app API and usage documentation

## Tech Stack

### Frontend
- React 19 + Vite
- React Router DOM
- Plain CSS

### Backend
- Flask + Flask-SQLAlchemy
- SQLite
- scikit-learn (ML model via joblib)
- Flask-CORS

## Project Structure
MedicalInsuracePricePrdiction/
├── backend/
│ ├── app.py # Flask API
│ ├── insurance_model.pkl # Trained ML model
│ ├── insurance.db # SQLite database
│ ├── seed_companies.py # Seed script for companies
│ └── requirements.txt
└── frontend/
├── src/
│ ├── component/ # React components
│ ├── App.jsx
│ └── main.jsx
└── package.json


## Getting Started

### Backend

```bash
cd backend
pip install -r requirements.txt
python app.py
```
Server runs at http://localhost:5001

Frontend
cd frontend
npm install
npm run dev

App runs at http://localhost:5173

API Endpoints
Method	Endpoint	Description
POST	/login	User login
POST	/register	User registration
GET	/companies	List all companies
POST	/companies	Add a company (admin)
POST	/predict	Predict insurance price
POST	/buy	Purchase a plan
POST	/user/dashboard	Get user purchase history
Default Admin Credentials


Username: admin
Password: admin123


Prediction Inputs
Field	Type	Values
age	number	e.g. 25
bmi	number	e.g. 28.5
children	number	0–5
smoker	boolean	0 = No, 1 = Yes
sex	boolean	0 = Female, 1 = Male
region	string	northeast, northwest, southeast, southwest
