# 🌦️ WOWW — Weather On World Wide  
> An Intelligent AI-powered Weather Forecasting and Rainfall Prediction Web App  

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.x-green?logo=flask)
![Machine Learning](https://img.shields.io/badge/Model-Regression%20%26%20SARIMA-orange)
![Google Gemini AI](https://img.shields.io/badge/Google%20Gemini-Integrated-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 🧠 Overview  

**WOWW (Weather On World Wide)** is a Flask-based intelligent **Weather Prediction System** that forecasts temperature, humidity, and rainfall probability using **Machine Learning**, **SARIMA Time Series Models**, and **AI integration with Google Gemini**.

This project combines **statistical forecasting**, **data-driven modeling**, and **natural language AI** to produce human-understandable, data-backed weather predictions for Indian cities.

---

## 🧩 Project Structure  

woww/
│
├── app.py # Flask backend & API routes
├── weather_predictor.py # ML + SARIMA + Probability logic
├── templates/
│ ├── final.html # Main UI
│ ├── wow.html # Prediction display
│ └── r.html # Result view
├── assets/
│ └── wback.mp4 # Background video
├── static/ # Optional CSS / JS
├── data/
│ ├── delhi.json
│ ├── mumbai.json
│ └── chennai.json # JSON weather data files
├── requirements.txt
└── README.md

---

## ⚙️ Installation & Setup  

### 🧰 Requirements  
- Python 3.10+
- Flask
- Pandas
- Scikit-learn
- Statsmodels
- Google Generative AI API (Gemini)

### 💻 Steps  

```bash
# Clone the repository
git clone https://github.com/<your-username>/woww.git
cd woww

# Create virtual environment
python -m venv venv
source venv/bin/activate       # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

## Run Flask app
python app.py
Open your browser and visit:
👉 http://127.0.0.1:5000/
🧬 Technologies Used
Category	Technology
Backend	Flask
Machine Learning	Scikit-learn, Statsmodels
Time Series	SARIMA (Seasonal ARIMA)
AI Integration	Google Gemini API
Data Handling	Pandas, NumPy
🧾 JSON Data Integration

Each city’s weather dataset is stored in .json format for easy access and modification.

Example:
Data Format	JSON
Evaluation Metric	RMSE (Root Mean Squared Error)
Frontend	HTML, CSS, J
Each file contains weather records across multiple years.

The app loads and preprocesses this data using Pandas before feeding it into the model.

You can easily add your own city dataset following the same structure.
📉 Model Design

The system uses a combination of SARIMA and probability models to predict weather outcomes.

## Acknowledgements

Google Gemini AI
 — AI support for intelligent insights

NASA POWER Project
 — Open weather dSata

Statsmodels
 — SARIMA model implementation

Flask
 — Backend framework
![Image](https://github.com/user-attachments/assets/5406bd35-c5a0-4b94-b963-2b24fc51864e)

![Image](https://github.com/user-attachments/assets/6feba4f6-c151-47ee-be93-0c3e0c38116e)

![Image](https://github.com/user-attachments/assets/0eb58aa3-11d2-426f-86c5-2f8c32f59105)
