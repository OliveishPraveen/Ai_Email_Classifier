# 🚀 AI Email Classifier

An intelligent email classification system that automatically categorizes emails and detects their urgency using a hybrid approach combining **DistilBERT deep learning models** and **rule-based filtering**.

---

## 📌 Overview

This project helps in managing emails efficiently by analyzing email content and predicting:

* 📂 **Category** → Complaint, Request, Feedback, Spam
* ⚡ **Urgency Level** → High, Medium, Low

It uses a **dual-model architecture**, where separate models are used for category classification and urgency detection to improve accuracy and scalability.

---

## 🧠 Key Features

* 🔍 Real-time email classification
* 🤖 DistilBERT-based NLP models
* ⚙️ Rule-based urgency detection
* 🌐 FastAPI backend for API handling
* 🎨 Streamlit frontend with dashboard
* 📊 Email analytics and visualization

---

## 🏗️ Project Structure

```
AI-Email-Classifier/
│
├── backend/
│   └── app.py
│
├── frontend/
│   └── app.py
│
├── models/
│   ├── category_model/
│   │   ├── config.json
│   │   ├── tokenizer.json
│   │   ├── tokenizer_config.json
│   │   └── category_encoder.pkl
│   │
│   ├── urgency_model/
│       ├── config.json
│       ├── tokenizer.json
│       ├── tokenizer_config.json
│       └── urgency_encoder.pkl
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ⚠️ Model Weights (Important)

Due to GitHub size limitations, **model weight files (`model.safetensors`) are not included** in this repository.

👉 Download them from here:
*(Add your Google Drive / HuggingFace link here)*

After downloading, place them in:

```
models/category_model/
models/urgency_model/
```

---

## 🔄 Workflow

1. User enters email text in Streamlit UI
2. Frontend sends request to FastAPI backend
3. Backend processes text using tokenizer
4. Text is passed into:

   * Category Model (DistilBERT)
   * Urgency Model (DistilBERT + Rule-based logic)
5. Predictions are decoded using label encoders
6. Final result returned as JSON
7. Displayed in frontend dashboard

---

## 🛠️ Tech Stack

* Python
* FastAPI
* Streamlit
* Hugging Face Transformers (DistilBERT)
* Scikit-learn
* Pandas & Plotly

---

## 🚀 How to Run

### 1️⃣ Clone the repository

```
git clone https://github.com/YOUR_USERNAME/ai-email-classifier.git
cd ai-email-classifier
```

---

### 2️⃣ Install dependencies

```
pip install -r requirements.txt
```

---

### 3️⃣ Run Backend

```
cd backend
uvicorn app:app --reload
```

---

### 4️⃣ Run Frontend

```
cd frontend
streamlit run app.py
```

---

## 📡 API Endpoint

**POST /classify**

Request:

```
{
  "email": "Your email content here"
}
```

Response:

```
{
  "category": "Complaint",
  "urgency": "High",
  "confidence": 0.92
}
```

---

## 🎯 Use Cases

* Customer support automation
* Email prioritization
* Helpdesk systems
* Business communication filtering

---

## 🚀 Future Improvements

* Batch email classification
* Database integration (MySQL)
* Model optimization
* Cloud deployment

---

## 👨‍💻 Author

**Praveen Solanki**

---

## 💡 Short Description (for GitHub top bar)

AI-powered email classifier using DistilBERT and rule-based logic to detect category and urgency with FastAPI backend and Streamlit frontend.
