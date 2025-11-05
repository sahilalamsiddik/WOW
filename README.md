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

🔹 SARIMA Model (Seasonal AutoRegressive Integrated Moving Average)

SARIMA is an advanced version of ARIMA that incorporates seasonality.

Formula:
𝑆
𝐴
𝑅
𝐼
𝑀
𝐴
(
𝑝
,
𝑑
,
𝑞
)
(
𝑃
,
𝐷
,
𝑄
)
𝑠
SARIMA(p,d,q)(P,D,Q)
s
	​


Where:

p → Number of autoregressive terms

d → Degree of differencing

q → Number of moving average terms

(P, D, Q) → Seasonal parameters

s → Length of seasonality (e.g., 12 for monthly data)

Model Equation:
𝑌
𝑡
=
𝑐
+
𝜙
1
𝑌
𝑡
−
1
+
⋯
+
𝜙
𝑝
𝑌
𝑡
−
𝑝
+
𝜃
1
𝜀
𝑡
−
1
+
⋯
+
𝜃
𝑞
𝜀
𝑡
−
𝑞
+
𝜀
𝑡
Y
t
	​

=c+ϕ
1
	​

Y
t−1
	​

+⋯+ϕ
p
	​

Y
t−p
	​

+θ
1
	​

ε
t−1
	​

+⋯+θ
q
	​

ε
t−q
	​

+ε
t
	​


Where:

𝑌
𝑡
Y
t
	​

 = predicted value

𝜙
ϕ = autoregressive coefficients

𝜃
θ = moving average coefficients

𝜀
𝑡
ε
t
	​

 = random error term

This model learns patterns in temperature and precipitation over time, producing accurate forecasts.

🔹 Model Evaluation — RMSE

To evaluate prediction accuracy, RMSE (Root Mean Squared Error) is used.

Formula:
𝑅
𝑀
𝑆
𝐸
=
1
𝑛
∑
𝑖
=
1
𝑛
(
𝑦
𝑖
−
𝑦
𝑖
^
)
2
RMSE=
n
1
	​

i=1
∑
n
	​

(y
i
	​

−
y
i
	​

^
	​

)
2
	​


Where:

𝑦
𝑖
y
i
	​

 = Actual value

𝑦
𝑖
^
y
i
	​

^
	​

 = Predicted value

𝑛
n = Total number of observations

✅ Lower RMSE = Better performance

🔹 Rain Probability Prediction

The model also calculates rainfall probability using a logistic function:

𝑃
(
𝑅
𝑎
𝑖
𝑛
)
=
1
1
+
𝑒
−
(
𝛽
0
+
𝛽
1
𝑇
+
𝛽
2
𝐻
+
𝛽
3
𝑃
)
P(Rain)=
1+e
−(β
0
	​

+β
1
	​

T+β
2
	​

H+β
3
	​

P)
1
	​


Where:

𝑇
T = Temperature

𝐻
H = Humidity

𝑃
P = Precipitation

𝛽
0
,
𝛽
1
,
𝛽
2
,
𝛽
3
β
0
	​

,β
1
	​

,β
2
	​

,β
3
	​

 = learned coefficients

If 
𝑃
(
𝑅
𝑎
𝑖
𝑛
)
>
0.5
P(Rain)>0.5, it predicts Rain.
Otherwise, No Rain.
🙏 Acknowledgements

Google Gemini AI
 — AI support for intelligent insights

NASA POWER Project
 — Open weather data

Statsmodels
 — SARIMA model implementation

Flask
 — Backend framework
