# 🧠 Sentiment Analysis API (FastAPI)

A lightweight Machine Learning–powered **Sentiment Analysis API** built using **FastAPI**.  
This project takes a text input and returns its **sentiment** (positive/negative/neutral) using a trained ML model (`sentiment.pkl`).

---

## 🚀 Features

- 🔥 FastAPI-powered high-performance backend  
- 🧠 Pre-trained ML model for sentiment prediction  
- 📡 REST API endpoints (`/predict`, `/heartbeat`)  
- 🧩 Modular and clean architecture  
- ⚡ Easy to deploy & easy to extend  
- ✔ JSON-based request/response  

---

## 📁 Project Structure

.
│ .env.example
│ pyproject.toml
│
├── app
│ ├── main.py
│ ├── api
│ │ └── routes
│ │ ├── heartbeat.py
│ │ ├── prediction.py
│ │ └── router.py
│ ├── core
│ │ ├── config.py
│ │ ├── event_handlers.py
│ │ ├── messages.py
│ │ └── security.py
│ ├── models
│ │ ├── heartbeat.py
│ │ ├── payload.py
│ │ └── prediction.py
│ └── services
│ ├── models.py
│ └── model_service.py
│
└── models
└── sentiment.pkl

yaml
Copy code

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```sh
git clone https://github.com/Himanshusekharsahoo/Sentiment-api-fastapi.git
cd Sentiment-api-fastapi
2️⃣ Create a virtual environment (recommended)
sh
Copy code
python -m venv venv
venv\Scripts\activate   # Windows
3️⃣ Install dependencies
Using pyproject:

sh
Copy code
pip install fastapi uvicorn scikit-learn numpy pandas python-dotenv
OR using requirements.txt:

sh
Copy code
pip install -r requirements.txt
▶️ Run the API Server
Use this command:

sh
Copy code
python -m uvicorn app.main:app --reload
Server runs at:

👉 http://127.0.0.1:8000
👉 Interactive Docs (Swagger): http://127.0.0.1:8000/docs
👉 ReDoc: http://127.0.0.1:8000/redoc

📡 API Endpoints
🔹 1. Heartbeat Check
GET /heartbeat

Response

json
Copy code
{
  "status": "alive",
  "message": "API is running"
}
🔹 2. Predict Sentiment
POST /predict

Request Body
json
Copy code
{
  "text": "I really love this product!"
}
Response (example)
json
Copy code
{
  "sentiment": "positive",
  "confidence": 0.92
}
🧠 ML Model Details
Format: pickle (sentiment.pkl)

Typical pipeline:

Text preprocessing (tokenizer/vectorizer)

Machine learning classifier (e.g., Logistic Regression / SVM / Naive Bayes)

You can replace the model with your own by updating the model_service.py.

📦 Build & Deployment
You can deploy on:

Render

Railway

AWS EC2

Azure App Service

Heroku (via container)

Docker

🤝 Contributing
Contributions are welcome!
Fork the repo, create a branch, commit, and open a PR.

📜 License
This project is released under the MIT License.
Feel free to modify and use it in your own projects.

👨‍💻 Author
Himanshu Sekhar Sahoo
📧 Email: work.himanshuse@gmail.com
🌐 GitHub: https://github.com/Himanshusekharsahoo

⭐ If you like this project, give it a star on GitHub! ⭐
