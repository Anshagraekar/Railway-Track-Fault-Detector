# 🚂 Railway Fault Detector using Deep Learning

## 📌 Project Overview

The **Railway Fault Detector** is an AI-powered system designed to identify faults in railway tracks using image classification. It uses a **VGG16-based Convolutional Neural Network (CNN)** integrated with a **FastAPI backend** and a **React frontend** to provide real-time predictions.

---

## 🎯 Features

* Upload railway track images
* Detect whether the track is **Safe ✅** or **Faulty ❌**
* Real-time prediction using deep learning
* User-friendly interface (React)
* Fast backend API (FastAPI)

---

## 🛠️ Tech Stack

### 🔹 Frontend

* React.js
* HTML, CSS, JavaScript

### 🔹 Backend

* FastAPI
* Python

### 🔹 Machine Learning

* TensorFlow / Keras
* VGG16 (Transfer Learning)
* NumPy, Pillow

---

## 🧠 Model Details

* Architecture: **VGG16 (Pretrained CNN)**
* Input Size: **224 × 224 RGB Images**
* Output:

  * Safe Track
  * Faulty Track
* Model File: `.h5`

---

## 📁 Project Structure

```
railway-fault-detector/
│
├── public/                 # React public assets
├── src/                    # React source code
├── server/                 # Backend (FastAPI)
│   ├── main.py
│   ├── requirements.txt
│   ├── model/
│   │   └── railway_fault_detector_vgg16.h5
│
├── package.json
├── README.md
├── .gitignore
```

---

## ⚙️ Installation & Setup

### 🔹 1. Clone the Repository

```
git clone https://github.com/your-username/railway-fault-detector.git
cd railway-fault-detector
```

---

### 🔹 2. Setup Backend

```
cd server
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

Run the backend:

```
uvicorn main:app --reload --port 3001
```

---

### 🔹 3. Setup Frontend

Open a new terminal:

```
npm install
npm start
```

Frontend runs on:

```
http://localhost:3000
```

---

## 🔗 API Endpoint

### POST `/predict/`

Upload an image and get prediction.

**Response Example:**

```
{
  "safe_probability": 0.92,
  "faulty_probability": 0.08,
  "status": "Track is Safe ✅"
}
```

---

## 📸 How It Works

1. User uploads image from frontend
2. Image is sent to FastAPI backend
3. Image is preprocessed (resized, normalized)
4. Model predicts class
5. Result displayed on UI

---

## ⚠️ Important Notes

* Make sure the model file is placed in:

```
server/model/
```

---

## 🚀 Future Improvements

* Improve model accuracy with larger dataset
* Add real-time video detection
* Deploy using cloud services (AWS / Render / Vercel)
* Add alert system for railway authorities

---

## 👨‍💻 Author

Ansh Agraekar, Mrunal Kanpillewar, Mayank Kumbhare, Swapnil Kottewar

---

## 📜 License

This project is for educational purposes.
