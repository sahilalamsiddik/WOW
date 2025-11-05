# 🌦️ WOWW — Intelligent Weather Prediction App

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.x-green?logo=flask)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Enabled-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

### 🧠 Smart, Accurate, and Beautifully Simple

**WOWW** (Weather On World Wide) is a Flask-based **AI-powered weather prediction web app** that forecasts temperature and rainfall probabilities for major Indian cities — using real-world data and ML modeling.  
Built to be lightweight, interactive, and intelligent, it provides both insights and predictions with a touch of style.

---

## 🚀 Features

✅ Predicts weather for multiple Indian cities  
✅ Determines whether it will rain on a specific date  
✅ Utilizes ML models trained on NASA POWER dataset (1985–2025)  
✅ Integrates Google Gemini AI for enhanced prediction and explanations  
✅ Responsive and video-based web interface  
✅ Simple to deploy locally or on cloud (Render, Heroku, etc.)

---


---

## 🧠 Code Architecture Overview

The app is built around **modular and maintainable architecture**, combining Flask’s simplicity with ML-backed predictions.

### 1️⃣ `app.py` — The Application Core
Handles:
- Web routes (`/`, `/predict`, `/rain`)
- User requests (city & date inputs)
- Communication with ML model (`weather_predictor.py`)
- JSON responses and template rendering

**Example Route:**
```python
@app.route('/predict', methods=['POST'])
def predict():
    city = request.form['city']
    date = request.form['date']
    prediction = forecast_for_date(city, date)
    return render_template('wow.html', result=prediction)


