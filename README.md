# SHL Assessment Recommender

A Streamlit-based application that takes a user query or job description and returns the most relevant SHL assessment from a provided catalog using semantic search.

---

## 🔍 Problem Statement

Given a dataset of SHL assessments, build an intelligent system that recommends the most relevant test based on a user-provided input query or job description. The goal is to simplify and optimize assessment selection for hiring and development purposes.

---

## 🛠️ Tech Stack

- **Frontend**: Streamlit
- **Backend**: Python, Pandas
- **Vector Search**: Sentence Transformers (`all-MiniLM-L6-v2`)
- **Data**: SHL assessment catalog (CSV)
- **Deployment**: Streamlit Cloud / Localhost

---

## 📊 Architecture

![System Architecture]("[C:\Users\User\Downloads\shl architecture.png](https://sdmntprsouthcentralus.oaiusercontent.com/files/00000000-a2cc-51f7-9314-aaa5f724252d/raw?se=2025-04-07T11%3A37%3A26Z&sp=r&sv=2024-08-04&sr=b&scid=0edb7c57-ec15-5cae-9044-a119b5cf8a38&skoid=7c382de0-129f-486b-9922-6e4a89c6eb7d&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-04-06T12%3A41%3A32Z&ske=2025-04-07T12%3A41%3A32Z&sks=b&skv=2024-08-04&sig=RJuWIcGfSt8DA/1XPQzPvGC1wVxQzX%2BrypDEMLJMxZg%3D)")
---


## 🚀 Features

- Uploads and processes SHL catalog data
- Embeds assessment descriptions using Sentence Transformers
- Accepts user input (query/job description)
- Returns top N matching assessments with scores
- Simple, responsive UI using Streamlit

---

## 📦 Installation

```bash
git clone https://github.com/yourusername/SHL-Assessment-Recommender.git
cd SHL-Assessment-Recommender
pip install -r requirements.txt
streamlit run app.py

POST /recommend
{
  "query": "We need a test for leadership and decision-making"
}

Response:
[
  {
    "assessment": "Situational Judgement Test",
    "score": 0.89,
    "link": "https://example.com/assessment"
  }
]


├── app.py
├── shl_catalog_detailed.csv
├── README.md
├── requirements.txt
└── architecture.png

