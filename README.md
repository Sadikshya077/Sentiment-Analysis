<div align="center">

# 🇳🇵 CNN-BiLSTM Based Target-Aspect Sentiment Analysis for Nepali Public Opinion Mining

### Deep Learning • Natural Language Processing • Target-Aspect Based Sentiment Analysis (TABSA)

A hybrid deep learning framework for analyzing **Nepali social media sentiment** from multilingual and code-mixed YouTube comments using **FastText, Transformer-based Target Detection, and CNN-BiLSTM**.

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange?style=for-the-badge&logo=tensorflow)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-yellow?style=for-the-badge)
![FastText](https://img.shields.io/badge/FastText-Language%20Identification-green?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-Open%20Source-black?style=for-the-badge&logo=github)

</div>

---

# 📖 Overview

Nepali social media comments are highly challenging for Natural Language Processing because they frequently contain:

- Nepali written in **Devanagari**
- **Romanized Nepali**
- English
- Code-mixed sentences
- Informal spellings and slang

Traditional sentiment analysis models often fail to understand these multilingual inputs.

This project introduces a **Target-Aspect Based Sentiment Analysis (TABSA)** pipeline capable of identifying the language, normalizing text, detecting opinion targets, and predicting both the **aspect** and **sentiment** associated with each target.

---

# 🚀 Key Features

- Language Identification using FastText
- Romanized Nepali → Devanagari Transliteration
- Transformer-based Target Detection
- CNN-BiLSTM Aspect Classification
- CNN-BiLSTM Sentiment Classification
- YouTube Comment Extraction using YouTube Data API
- Modular NLP Pipeline
- Support for multilingual and code-mixed Nepali text

---

# 🏗 System Architecture

```
                    YouTube Comments
                           │
                           ▼
          Language Identification (FastText)
                           │
                           ▼
     Romanized → Devanagari Transliteration
                           │
                           ▼
      Transformer-based Target Detection
                           │
                           ▼
            CNN + Bidirectional LSTM
                           │
            ┌──────────────┴──────────────┐
            ▼                             ▼
   Aspect Classification        Sentiment Classification
```

---

# 🧠 Model Architecture

The proposed sentiment classifier combines the strengths of two neural architectures.

### CNN

- Captures local semantic patterns
- Learns important n-gram features
- Extracts discriminative representations

### Bidirectional LSTM

- Learns contextual dependencies
- Understands long-range relationships
- Processes text in both forward and backward directions

The combined CNN-BiLSTM architecture effectively models Nepali social media text, improving both aspect detection and sentiment prediction.

---

# 🔄 Project Workflow

```
Collect YouTube Comments
        │
        ▼
Detect Language
        │
        ▼
Transliterate Romanized Nepali
        │
        ▼
Detect Opinion Target
        │
        ▼
CNN Feature Extraction
        │
        ▼
BiLSTM Context Learning
        │
        ▼
Aspect Prediction
        │
        ▼
Sentiment Prediction
```

---

# 💻 Technology Stack

| Category | Technologies |
|-----------|--------------|
| Programming | Python |
| Deep Learning | TensorFlow, Keras |
| NLP | Hugging Face Transformers, FastText |
| Machine Learning | Scikit-learn |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib |
| API | YouTube Data API v3 |
| Version Control | Git & GitHub |
| Development | VS Code, Google Colab |

---

# 📂 Repository Structure

```
.
├── NLP-project/
│   ├── comment_extractor.py
│   ├── main.py
│   ├── pipeline.py
│   ├── registry.py
│   └── ml/
│       ├── base.py
│       ├── devanagari.py
│       ├── language_identifier.py
│       ├── target_model.py
│       └── transliteration_model.py
│
├── models/
│   ├── devanagari_models/
│   ├── target_model/
│   ├── translation_model/
│   └── transliteration_model/
│
├── .gitignore
└── README.md
```

---

# 📊 Highlights

✔ Developed a multilingual NLP pipeline for Nepali social media.

✔ Built a hybrid CNN-BiLSTM deep learning model.

✔ Integrated FastText language identification for multilingual inputs.

✔ Implemented Romanized Nepali transliteration.

✔ Incorporated Transformer-based target detection.

✔ Automated YouTube comment collection using YouTube Data API.

✔ Designed the system using a modular architecture for extensibility.

---

# 📦 Large Model Files

GitHub limits files larger than **100 MB**.

Therefore, the following pretrained models are **not included** in this repository:

- FastText Language Identification Model
- Transformer Target Detection Model (`model.safetensors`)

Only configuration files and lightweight models are included.

---

# 🔮 Future Improvements

- Web application deployment
- Real-time sentiment dashboard
- Explainable AI (XAI)
- Named Entity Recognition enhancement
- Larger multilingual datasets
- Improved target extraction
- Model optimization for faster inference

---

# 👩‍💻 Authors

- **Sadikshya Adhikari**
- **Nirika Lamichhane**
- **Ankita Shah**
- **Pooja Kapari**

### Supervisor

**Er. Rajad Shakya**

Department of Computer Engineering  
Thapathali Engineering Campus  
Tribhuvan University

---

# 📄 License

This project was developed for academic research and educational purposes.

---

<div align="center">

### ⭐ If you found this project interesting, consider giving it a star!

</div>