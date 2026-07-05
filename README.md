# Applied ML Case Studies

## Overview
This repository contains applied machine learning prototypes exploring financial news sentiment analysis and organizational resource optimization. These are separate from this author's primary energy/engineering-focused work (see [energy-ml-prototypes](https://github.com/Sina-33/energy-ml-prototypes)) and are kept here as general applied-ML case studies.

## Research / Engineering Motivation
Each case study explores applying standard ML/NLP techniques to a decision-support problem outside the energy domain: using BERT-based sentiment analysis on financial news to inform investment decisions, and using historical failure data to inform organizational resource allocation.

## Methods
- BERT-based text classification (fine-tuned `bert-base-uncased`) for financial news sentiment
- Flask REST API for model serving
- Predictive modeling and resource optimization for organizational data

## Features
- **AI Decision Assistant for Investors**: fetches financial news and classifies sentiment using a fine-tuned BERT model
- **Organizational Learning and Resource Optimization**: predicts startup/organizational failure risk and suggests resource allocation, served via a Flask API + dashboard

## Results / Outputs
See each subfolder's own README for case-study-specific details.

## Repository Structure
```
.
├── AI Decision Assistant for Investors/
│   ├── app.py               # Entry point
│   ├── fetch_news.py        # News API client
│   ├── bert_model.py        # BERT inference
│   ├── train_model.py       # Fine-tuning script
│   └── requirements.txt
└── Organizational Learning and Resource Optimization/
    ├── app/                  # Flask API + dashboard
    ├── models/               # Failure prediction + resource optimization
    └── data/                 # failed_startups.csv
```

## How to Run
Each case study has its own `requirements.txt`:
```bash
cd "AI Decision Assistant for Investors"
pip install -r requirements.txt
```

## Technologies Used
Python, Flask, Hugging Face Transformers (BERT), scikit-learn, pandas

## Limitations
- **`AI Decision Assistant for Investors/app.py` uses a placeholder API key** (`NEWS_API_KEY = "your_api_key_here"`) and will not run end-to-end without a user-supplied [NewsAPI](https://newsapi.org/) key. No real key is committed to this repository.
- The organizational failure dataset (`failed_startups.csv`) is limited in scope; results should be treated as illustrative, not statistically robust.
- These are prototypes for exploring applied ML workflows, not validated decision-support tools.

## Future Improvements
- Add a `.env.example` documenting required API keys instead of a placeholder in source
- Expand and validate the failure-prediction dataset
- Add evaluation metrics and a proper train/test split report for the BERT sentiment model

## Author
Sina Mohammadi
