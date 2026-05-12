## Overview
The **Netflix PM Qualitative Analysis Tool** is a Python-based interactive dashboard designed for Product Managers. It automates the process of analyzing large datasets of user feedback (in this case, 150,000+ Netflix app reviews) to extract actionable product insights, measure user sentiment, and automatically generate backlog recommendations.

This tool bridges the gap between raw qualitative data and structured product strategy using Natural Language Processing (NLP).

## 🚀 Features
* **Star Rating Distribution:** Visualizes the overall health of the app using Matplotlib with a custom `viridis` color palette.
* **Sentiment Analysis:** Uses `TextBlob` to categorize user reviews into Positive, Negative, or Neutral sentiments (`viridis_r` color mapped).
* **Topic Modeling (LDA):** Leverages `scikit-learn's Latent Dirichlet Allocation to group thousands of reviews into distinct product themes (e.g., UI/UX bugs, content library, streaming quality) while filtering out common stop words.
* **Feature Word Clouds:** Generates visual summaries of the most frequently mentioned keywords per theme.
* **Automated PM Recommendations:** Synthesizes theme keywords, average sentiment, and star ratings into actionable product steps (e.g., "High Priority Fix", "Needs Discovery", "Promote & Maintain").
* **PDF Export:** Allows PMs to download a clean, formatted PDF report of the insights for stakeholder meetings using `fpdf`.

## 🛠️ Tech Stack
* **Frontend:** [Streamlit](https://streamlit.io/)
* **Data Manipulation:** Pandas, NumPy
* **NLP & Machine Learning:** Scikit-learn (CountVectorizer, LDA), TextBlob
* **Data Visualization:** Matplotlib, WordCloud
* **Document Generation:** FPDF

## 📂 Project Structure
```text
├── app.py                   # Main Streamlit application script
├── netflix_reviews.csv      # Dataset containing app reviews and ratings
├── README.md                # Project documentation
└── requirements.txt         # Python dependencies
