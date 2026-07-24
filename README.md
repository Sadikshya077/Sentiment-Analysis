# CNN-BiLSTM Based Target-Aspect Sentiment Analysis for Nepali Public Opinion Mining

A deep learning framework for **Target-Aspect Based Sentiment Analysis (TABSA)** on Nepali YouTube comments. This project combines language identification, transliteration, target detection, and sentiment classification to analyze public opinion from multilingual and code-mixed social media data.

---

## Overview

Social media comments in Nepal frequently contain:

- Nepali written in Devanagari
- Romanized Nepali
- English
- Code-mixed text

Traditional sentiment analysis models struggle with this linguistic diversity.

This project proposes a hybrid pipeline that first normalizes multilingual input and then performs **target-specific aspect and sentiment analysis** using a CNN-BiLSTM model.

---

## Features

- Language Identification using FastText
- Romanized Nepali → Devanagari Transliteration
- Target Detection using a pretrained Transformer model
- Target-Aspect Based Sentiment Analysis
- CNN-BiLSTM deep learning architecture
- YouTube comment extraction using YouTube Data API
- Modular inference pipeline

---

## System Pipeline

```text
YouTube Comments
        │
        ▼
Language Identification (FastText)
        │
        ▼
Transliteration (Romanized → Devanagari)
        │
        ▼
Target Detection
        │
        ▼
CNN-BiLSTM
        │
        ├── Aspect Classification
        └── Sentiment Classification
```

---

## Tech Stack

| Category | Technologies |
|----------|--------------|
| Language | Python |
| Deep Learning | TensorFlow, Keras |
| NLP | Hugging Face Transformers, FastText |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Data Collection | YouTube Data API v3 |
| Development | VS Code, Google Colab |
| Version Control | Git & GitHub |

---

## Project Structure

```
.
├── NLP-project/
│   ├── main.py
│   ├── pipeline.py
│   ├── registry.py
│   ├── comment_extractor.py
│   └── ml/
│       ├── language_identifier.py
│       ├── transliteration_model.py
│       ├── target_model.py
│       ├── devanagari.py
│       └── base.py
│
├── models/
│   ├── devanagari_models/
│   ├── translation_model/
│   ├── transliteration_model/
│   └── target_model/
│
└── README.md
```

---

## Model Architecture

The sentiment prediction model combines:

- CNN for local feature extraction
- Bidirectional LSTM for contextual sequence learning
- Dual-output prediction
  - Aspect Classification
  - Sentiment Classification

This architecture captures both local semantic patterns and long-range contextual dependencies in Nepali text.

---

## Workflow

1. Collect YouTube comments.
2. Detect input language.
3. Transliterate Romanized Nepali into Devanagari.
4. Detect opinion target.
5. Extract semantic features using CNN.
6. Learn contextual dependencies using BiLSTM.
7. Predict:
   - Target Aspect
   - Sentiment (Positive / Neutral / Negative)

---

## Repository Contents

This repository includes:

- Source code
- Model configuration files
- Tokenizers
- Small trained models

Large pretrained models have been excluded because they exceed GitHub's file size limit.

---

## Future Improvements

- Deploy as a web application
- Improve target extraction accuracy
- Support additional Nepali dialects
- Real-time sentiment monitoring dashboard
- Explainable AI (XAI) integration

---

## Authors

- Sadikshya Adhikari
- Nirika Lamichhane
- Ankita Shah
- Pooja Kapari

Supervisor:
**Er. Rajad Shakya**

---

## License

This project was developed for academic and research purposes.