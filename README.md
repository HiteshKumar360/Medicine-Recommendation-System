# 🩺 Medicine Recommendation System

[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.x-black?style=for-the-badge&logo=flask)](https://flask.palletsprojects.com)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=for-the-badge&logo=scikit-learn)](https://scikit-learn.org)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

An ML-powered web application that predicts diseases from user-entered symptoms and delivers personalized health recommendations — including medications, precautions, diet plans, and workouts — using a trained **Support Vector Machine (SVM)** classifier.

---

## 📸 Preview

> Enter your symptoms → Get instant disease prediction + full health plan

---

## ✨ Features

- 🔍 **Disease Prediction** — Predicts from 40+ diseases based on 132 possible symptoms
- 💊 **Medication Suggestions** — Recommends relevant medications for the predicted condition
- 🥗 **Diet Plans** — Provides tailored dietary recommendations
- 🏋️ **Workout Advice** — Suggests appropriate physical activities
- 🛡️ **Precautionary Measures** — Lists actionable steps to manage or prevent the condition
- 🌐 **User-Friendly Web Interface** — Built with Flask and Jinja2 templates

---

## 🛠️ Tech Stack

| Layer       | Technology                        |
|-------------|-----------------------------------|
| Backend     | Python, Flask                     |
| ML Model    | Scikit-learn (SVM Classifier)     |
| Data        | Pandas, NumPy                     |
| Frontend    | HTML, CSS (Jinja2 Templates)      |
| Model Store | Pickle                            |

---

## 📁 Project Structure

```
Medicine-Recommendation-System/
│
├── dataset/                  # CSV datasets for symptoms, diseases, etc.
│   ├── symtoms_df.csv
│   ├── precautions_df.csv
│   ├── workout_df.csv
│   ├── description.csv
│   ├── medications.csv
│   └── diets.csv
│
├── models/
│   └── svc.pkl               # Trained SVM model
│
├── static/                   # CSS, JS, images
├── templates/                # HTML templates (Jinja2)
│   ├── index.html
│   ├── about.html
│   ├── contact.html
│   ├── developer.html
│   └── blog.html
│
├── main.py                   # Flask application entry point
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- pip

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/HiteshKumar360/Medicine-Recommendation-System.git
cd Medicine-Recommendation-System

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the application
python main.py
```

### Access

Open your browser and navigate to:
```
http://127.0.0.1:5000
```

---

## 📊 How It Works

```
User Input (symptoms)
        ↓
Symptom Encoding → 132-dim binary vector
        ↓
SVM Classifier → Predicts Disease
        ↓
Dataset Lookup → Fetch recommendations
        ↓
Output: Disease Info + Medications + Diet + Precautions + Workout
```

1. User enters comma-separated symptoms (e.g., `fever, headache, nausea`)
2. Symptoms are encoded into a binary feature vector matching the model's input shape
3. The trained SVM classifier predicts the most likely disease
4. Helper functions query CSV datasets to fetch matching records
5. All results are rendered dynamically on the web page

---

## 🤖 ML Model Details

| Property        | Value                          |
|-----------------|-------------------------------|
| Algorithm       | Support Vector Machine (SVM)  |
| Input Features  | 132 symptoms (binary encoded) |
| Output Classes  | 41 diseases                   |
| Training Data   | Symptom-disease dataset        |
| Serialization   | Pickle (.pkl)                 |

---

## 📋 Supported Diseases (Sample)

| # | Disease              | # | Disease             |
|---|----------------------|---|---------------------|
| 1 | Fungal Infection     | 2 | Allergy             |
| 3 | GERD                 | 4 | Diabetes            |
| 5 | Hypertension         | 6 | Migraine            |
| 7 | Malaria              | 8 | Dengue              |
| 9 | Tuberculosis         | 10 | Common Cold        |
| 11 | Pneumonia           | 12 | Heart Attack        |
| ...| *(41 total)*        |   |                     |

---

## 🤝 Contributing

Contributions are welcome! Here's how:

```bash
# Fork the repo, then:
git checkout -b feature/your-feature-name
git commit -m "Add your feature"
git push origin feature/your-feature-name
# Open a Pull Request
```

---

## ⚠️ Disclaimer

> This application is intended for **educational and informational purposes only**.  
> It is **not** a substitute for professional medical advice, diagnosis, or treatment.  
> Always consult a qualified healthcare provider for any medical concerns.

---

## 👨‍💻 Developer

**Hitesh Kumar**  
GitHub: [@HiteshKumar360](https://github.com/HiteshKumar360)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">Made with ❤️ for learning and healthcare innovation</p>
