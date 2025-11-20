# 🧠 Sentiment Analysis API (FastAPI)

A lightweight Machine Learning–powered **Sentiment Analysis API** built using **FastAPI**.  
This project takes a text input and returns its **sentiment** (positive / negative / neutral) using a trained ML model (`sentiment.pkl`).

---

## 🚀 Features

- 🔥 High-performance FastAPI backend  
- 🧠 Pre-trained machine learning sentiment model  
- 📡 REST endpoints (`/predict`, `/heartbeat`)  
- 🧩 Clean modular architecture  
- ⚡ Easy to deploy and extend  
- ✔ Simple JSON request/response  

---

## 📁 Project Structure

```

.
│   .env.example
│   pyproject.toml
│   requirements.txt
│
├── app
│   ├── main.py
│   ├── api
│   │   └── routes
│   │       ├── heartbeat.py
│   │       ├── prediction.py
│   │       └── router.py
│   ├── core
│   │   ├── config.py
│   │   ├── event_handlers.py
│   │   ├── messages.py
│   │   └── security.py
│   ├── models
│   │   ├── heartbeat.py
│   │   ├── payload.py
│   │   └── prediction.py
│   └── services
│       ├── models.py
│       └── model_service.py
│
└── models
└── sentiment.pkl

````

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```sh
git clone https://github.com/Himanshusekharsahoo/Sentiment-api-fastapi.git
cd Sentiment-api-fastapi
````

### 2️⃣ Create a virtual environment

```sh
python -m venv venv
venv\Scripts\activate   # Windows
```

### 3️⃣ Install dependencies (Choose ONE)

#### ✔ Using pyproject.toml (manual)

```sh
pip install fastapi uvicorn scikit-learn numpy pandas python-dotenv
```

#### ✔ OR using requirements.txt

```sh
pip install -r requirements.txt
```

---

## ▶️ Run the API Server

```sh
python -m uvicorn app.main:app --reload
```

### Server will run at:

* 👉 **[http://127.0.0.1:8000](http://127.0.0.1:8000)**
* 👉 **Swagger Docs:** [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
* 👉 **ReDoc:** [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## 📡 API Endpoints

### 🔹 **1. Heartbeat Check**

**GET** `/heartbeat`

#### Response:

```json
{
  "status": "alive",
  "message": "API is running"
}
```

---

### 🔹 **2. Predict Sentiment**

**POST** `/predict`

#### Request Body:

```json
{
  "text": "I really love this product!"
}
```

#### Response Example:

```json
{
  "sentiment": "positive",
  "confidence": 0.92
}
```

---

## 🧠 ML Model Details

* Model Format: **pickle (`sentiment.pkl`)**
* Pipeline includes:

  * Text preprocessing (tokenization / vectorization)
  * ML classifier (e.g., Logistic Regression / SVM / Naive Bayes)

You can replace the model anytime by updating `model_service.py`.

---

## 📦 Deployment Options

You can deploy this API easily on:

* Render
* Railway
* AWS EC2
* Azure App Service
* Heroku (via Docker)
* Docker containers

---

## 🤝 Contributing

Contributions are welcome!
Fork the repo → create a branch → commit → open a PR.

---

## 📜 License

This project is licensed under the **MIT License**.
Feel free to use, modify, and share.

---

## 👨‍💻 Author

**Himanshu Sekhar Sahoo**</br>
📧 Email: [work.himanshuse@gmail.com](mailto:work.himanshuse@gmail.com)</br>
🌐 GitHub: [https://github.com/Himanshusekharsahoo](https://github.com/Himanshusekharsahoo)

---

⭐ *If you like this project, don't forget to star the repository!* ⭐
