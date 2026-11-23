# Health Insight AI Analyser

A symptom-based disease prediction and health recommendation web application built with **Python**, **Flask**, **Scikit-Learn**, and **Bootstrap**[cite: 1, 2]. Users can enter symptoms (via text input or browser speech recognition) to receive a predicted condition along with an overview, precautions, medications, workout tips, and dietary guidance[cite: 1, 6].

## Features

- **Symptom-to-Disease Prediction:** Maps 132 encoded symptoms into a feature vector and predicts potential conditions using a trained Support Vector Classifier (`svc.pkl`)[cite: 1].
- **Voice Input Support:** Includes browser-based speech recognition (`webkitSpeechRecognition`) on the main prediction interface[cite: 6].
- **Holistic Health Guidance:** Displays modal views for predicted disease, description, precautions, medications, workouts, and diet recommendations loaded from CSV datasets[cite: 1, 6].
- **Multi-Page Web Interface:** Includes routes and templates for Home/Predict (`/` and `/predict`), About (`/about`), Contact (`/contact`), Developer (`/developer`), and Blog (`/blog`)[cite: 1, 2, 3, 4, 5, 6].
- **Model Training Pipeline:** Includes `model_training.py` comparing SVC, Random Forest, Gradient Boosting, K-Nearest Neighbors, and Multinomial Naive Bayes before exporting the SVC model[cite: 7].

## Tech Stack

- **Backend:** Flask, Python[cite: 1]
- **Machine Learning & Data:** Scikit-Learn, Pandas, NumPy, Pickle[cite: 1, 7]
- **Frontend:** HTML5, CSS3, Bootstrap 5, JavaScript (Web Speech API)[cite: 6]

## Project Structure

```text
├── main.py                  # Flask application and prediction routes
├── model_training.py        # Model comparison and SVC training script
├── models/
│   └── svc.pkl              # Serialized Support Vector Classifier model
├── datasets/
│   ├── symtoms_df.csv
│   ├── precautions_df.csv
│   ├── workout_df.csv
│   ├── description.csv
│   ├── medications.csv
│   └── diets.csv
└── templates/
    ├── index.html
    ├── about.html
    ├── blog.html
    ├── contact.html
    └── developer.html
