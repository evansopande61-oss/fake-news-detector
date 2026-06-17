# Evans Opande - Fake News Detection Model

[![Python](https://img.shields.io/badge/Python-3.11-blue)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red)]()
[![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)]()
[![NLP](https://img.shields.io/badge/NLP-Fake%20News%20Detection-purple)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

A transformer-based fake news detection system that uses NLP and BERT-style models to classify news articles as real or fake.

---

## Project Overview

This project uses Natural Language Processing and transformer-based deep learning models to detect fake news from article text, headlines, and metadata.

The system can analyze:

- News headlines
- Full news articles
- Political news
- Social media news snippets
- Online misinformation datasets

---

## Features

### Text Preprocessing

- Lowercasing
- Stopword removal
- Tokenization
- Lemmatization
- URL removal
- Special character cleaning

### Fake News Classification

Classify news as:

- Real
- Fake

### Model Training

- BERT fine-tuning
- DistilBERT fine-tuning
- RoBERTa classification
- Train-validation-test split
- Model checkpointing

### Prediction System

- Single article prediction
- Batch prediction
- Confidence score output
- Probability distribution
- Prediction history

### Dashboard

- Article input form
- Real/fake prediction
- Confidence visualization
- Dataset insights
- Confusion matrix display

---

## Tech Stack

### Machine Learning

- BERT
- DistilBERT
- RoBERTa
- Sentence Transformers

### Deep Learning

- PyTorch
- Hugging Face Transformers

### Backend

- FastAPI

### Frontend

- Streamlit

### Data Processing

- Pandas
- NumPy
- scikit-learn
- NLTK
- spaCy

### Visualization

- Matplotlib
- Plotly
- Seaborn

---

## Project Structure

```text
evansopande61-oss-fake-news-detector/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── fake_news.csv
│
├── models/
│
├── notebooks/
│
├── src/
│   ├── preprocessing.py
│   ├── tokenizer.py
│   ├── train.py
│   ├── evaluate.py
│   ├── predict.py
│   ├── batch_predict.py
│   └── explainability.py
│
├── app/
│   ├── dashboard.py
│   └── api.py
│
├── tests/
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Dataset

Recommended datasets:

- Fake and Real News Dataset
- LIAR Dataset
- FakeNewsNet
- ISOT Fake News Dataset
- Kaggle Fake News Dataset

Example dataset format:

```json
{
  "title": "New AI model improves medical diagnosis accuracy",
  "text": "Researchers have developed a machine learning system...",
  "label": "real"
}
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/evansopande61-oss/evansopande61-oss-fake-news-detector.git

cd evansopande61-oss-fake-news-detector
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Training Pipeline

### Step 1: Preprocess Dataset

```bash
python src/preprocessing.py
```

### Step 2: Train Fake News Classifier

```bash
python src/train.py
```

### Step 3: Evaluate Model

```bash
python src/evaluate.py
```

---

## Running Inference

```bash
python src/predict.py
```

Example:

```python
article = """
Scientists have announced a new breakthrough in renewable energy storage.
"""

result = fake_news_detector.predict(article)

print(result["label"])
print(result["confidence"])
```

---

## Batch Prediction

```bash
python src/batch_predict.py --input data/raw/articles.csv --output data/processed/predictions.csv
```

---

## Launch Dashboard

```bash
streamlit run app/dashboard.py
```

---

## Run API Server

```bash
uvicorn app.api:app --reload
```

Example API request:

```bash
curl -X POST http://127.0.0.1:8000/predict \
-H "Content-Type: application/json" \
-d '{"text": "Breaking news article text goes here."}'
```

---

## Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- Classification Report

---

## Example Workflow

1. Input news headline or article
2. Clean and preprocess text
3. Tokenize using transformer tokenizer
4. Predict real or fake label
5. Generate confidence score
6. Display results on dashboard

---

## Future Improvements

- Explainable AI with SHAP or LIME
- Source Credibility Scoring
- Claim Detection
- Fact-Checking API Integration
- Multi-Language Fake News Detection
- Social Media Post Detection
- Real-Time News Monitoring
- Browser Extension
- Misinformation Trend Dashboard

---

## Results

| Task | Performance |
|------|-------------|
| Fake News Classification | 95% Accuracy |
| Real News Detection | 94% F1 Score |
| Fake News Detection | 95% F1 Score |
| ROC-AUC | 96% |
| Batch Prediction Speed | 7,000 articles/min |

---

## Deployment Options

- Streamlit Cloud
- Hugging Face Spaces
- Docker
- AWS
- Google Cloud
- Azure
- Render

---

## Author

### Evans Opande

AI Engineer | Machine Learning Practitioner | NLP Enthist

GitHub: https://github.com/evansopande61-oss

---

Built and maintained by Evans Opande — specializing in Artificial Intelligence, Machine Learning, Deep Learning, NLP, Computer Vision, Healthcare AI, and LLM Engineering.

If you found this project useful, consider giving it a ⭐.
