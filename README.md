# Fake News Detection

Welcome to the Fake News Detection project! This repository provides a robust, end-to-end pipeline to detect fake news using classic machine learning models, with a seamless web experience powered by Streamlit.

---

## 🚀 Live Demo

**Try the deployed app here:**  
[Fake News Detection Streamlit App](https://fake-news-detection-kt66btejr8bk7ws8rjdted.streamlit.app/)

---

## 📂 Project Structure

```
fake-news-detector/
│
├── .venv/                  # Python virtual environment
├── fake_news_env/          # Additional env configs
├── newenv/                 # Alternative env configs
├── templates/              # Streamlit or web templates
├── .gitignore
├── app.ipynb               # Jupyter Notebook for EDA & training
├── app.py                  # Streamlit app source code
├── Fake.csv                # Fake news data
├── True.csv                # Real news data
├── ir_model.jb             # Trained ML model (joblib)
├── vectorizer.jb           # TF-IDF vectorizer (joblib)
├── requirements.txt        # Dependencies
```

---

## 🧑‍💻 Models Used

This project leverages the following machine learning models for fake news classification:

- **Logistic Regression**  
  *Accuracy: 98.65%*
- **Decision Tree Classifier**  
  *Accuracy: 99.61%*
- **Random Forest Classifier**  
  *Accuracy: 99.11%*

All models were trained on a labeled dataset from Kaggle, utilizing TF-IDF vectorized text features.

---

## 🗃️ Dataset

- **Source:** [Kaggle - Fake and Real News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- **Files:** `Fake.csv` (fake news), `True.csv` (real news)
- **Features:** `title`, `text`, and `label` (fake/real)

---

## ⚙️ Pipeline Overview

1. **Data Preprocessing**
   - Merge and clean `Fake.csv` and `True.csv`
   - Remove noise, punctuation, and stopwords
   - Text vectorization with TF-IDF

2. **Model Training**
   - Train and validate Logistic Regression, Decision Tree, and Random Forest models
   - Evaluate with accuracy and confusion matrix
   - Save best model and vectorizer

3. **Web App**
   - User inputs news content via Streamlit (`app.py`)
   - Input is preprocessed and classified in real-time

---

## 🏁 How to Use

### Installation

```bash
git clone https://github.com/<your-username>/fake-news-detector.git
cd fake-news-detector
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Launch Streamlit App

```bash
streamlit run app.py
```

### Jupyter Notebook

Explore all experiments and EDA in `app.ipynb`.

---

## 📊 Results & Evaluation

Below are the confusion matrices and reported accuracies for each model, showcasing strong predictive performance and minimal misclassification:

### Logistic Regression  
**Accuracy:** 98.65%

![Confusion Matrix - Logistic Regression](2)

---

### Decision Tree Classifier  
**Accuracy:** 99.61%

![Confusion Matrix - Decision Tree](3)

---

### Random Forest Classifier  
**Accuracy:** 99.11%

![Confusion Matrix - Random Forest](4)

---

All models delivered excellent accuracy, with the Decision Tree Classifier achieving the highest score. The confusion matrices above make it clear: both fake and real news are distinguished with high precision, as reflected in the very low number of misclassifications.

---

## 🌐 Deployment

- **Framework:** Streamlit
- **Live Demo:** [Streamlit App](https://fake-news-detection-kt66btejr8bk7ws8rjdted.streamlit.app/)
- **How to Deploy:**  
  The app is ready for cloud deployment (Streamlit Cloud, Hugging Face Spaces, etc.) and runs locally with `app.py`.

---

## 🤝 Contributing

Pull requests and suggestions are warmly welcome!  
Open an issue or PR for enhancements, bugfixes, or questions.

---

## 📄 License

This project is open source. Please specify your license terms here (e.g., MIT).

---

## 📬 Contact

For questions, collaborations, or feedback, reach out via GitHub issues.

---
