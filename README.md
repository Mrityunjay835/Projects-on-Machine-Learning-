# 🏥 Healthcare Query Chatbot

A conversational AI chatbot designed for **hospital-based queries** such as:
- Drug information
- Blood pressure inquiries
- Patient ID validation
- Pharmacy search
- Hospital search
- General medical assistance queries

This chatbot uses **Natural Language Processing (NLP)** with **NLTK**, and a Neural Network model built using **TensorFlow/Keras**, trained on custom intents defined in `intents.json`.

---

## 🚀 Features

✔ Conversational medical query assistance  
✔ Pre-defined hospital intents (Drug Inquiry, Pharmacy Search, Patient ID, etc.)  
✔ Uses **Bag-of-Words (BoW)** and **lemmatization** for text processing  
✔ Neural network classification model  
✔ Intent-based response generation  
✔ Easily expandable with more intents

---

## 🧰 Tech Stack

| Component | Technology |
|----------|------------|
| Language | Python |
| NLP Processing | NLTK |
| AI/ML Framework | TensorFlow / Keras |
| Data Storage | JSON (for intents), Pickle for saved vocab + labels |
| Model | Feed-Forward Neural Network |

---

## 📂 Project Structure

📦 Healthcare-Chatbot
│
├── intents.json # predefined training dataset (intents & responses)
├── chatbot_Application_model.h5 # saved ML model
├── words.pkl # vocabulary (preprocessed words)
├── labels.pkl # output class labels
├── train_chatbot.py # training script
└── chatbot_response.py # chat interaction script



---
## 🎯 How It Works

1. Tokenizes and lemmatizes input text using **NLTK**
2. Converts text into Bag-of-Words vector
3. Model predicts intent category using Neural Network
4. Bot responds according to matching intent in `intents.json`

---

## 🛠️ Setup & Installation
[git clone https://github.com/Mrityunjay835/Projects-on-Machine-Learning-]
cd Healthcare-Chatbot
pip install -r requirements.txt

cd Healthcare-Chatbot
pip install -r requirements.txt

cd Healthcare-Chatbot
pip install -r requirements.txt

## Download required NLTK data:
import nltk
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('omw-1.4')

## 💬 Running the Chatbot
python ChatBot_Application.py


## 🔐 Disclaimer

This is not a replacement for professional medical advice.
It is designed primarily for informational and internal hospital workflow queries only.

## 👨‍💻 Author

Mrityunjay Kumar
mrityunjaykumar835@gmail.com
