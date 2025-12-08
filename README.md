# Multi-Source Review Mining: Pros, Cons, and Product Similarity
## Author: Sarvin Shahir

<<<<<<< HEAD
This project analyzes beauty product reviews from multiple retailers — Sephora, Ulta, and Shoppers Drug Mart — using Natural Language Processing (NLP) techniques to extract benefits, disadvantages, and product similarity.  
A Streamlit application is included for interactive product comparison.

---

## 📁 Project Structure
**data/** → Raw and processed CSV files  
**notebooks/** → All analysis and modeling notebooks  
**outputs/** → Heatmaps, similarity plots, and visualizations  
**app.py** → Streamlit app for product comparison  

---

## 📓 Notebooks Overview

| Notebook | Purpose |
|----------|---------|
| `1_dataset_collection.ipynb` | Collect and merge reviews from Sephora, Ulta, Shoppers |
| `2_dataset_foundation.ipynb` | Foundation review dataset processing |
| `3_dataset_moisturizer.ipynb` | Moisturizer review dataset processing |
| `4_EDA.ipynb` | Data cleaning and exploratory analysis |
| `5_TF_IDF.ipynb` | Baseline feature extraction + classical models |
| `6_opinion_mining.ipynb` | Pros/cons extraction experiments |
| `7_BERT.ipynb` | BERT model for rating prediction |
| `8_BART.ipynb` | BART for text summarization and extraction |
| `9_KeyBert.ipynb` | Keyword extraction trials |
| `10_GPT_4o_mini.ipynb` | Benefit & disadvantage extraction with GPT |
| `11_Comparison.ipynb` | Comparison of extracted benefits across brands |
| `12_before_streamlit.ipynb` | Generate files for the Streamlit app |

---

## 📊 Dataset Summary
- Reviews collected for **12 beauty products** (foundations + moisturizers)  
- ~1,000+ total reviews  
- Extracted metadata includes:  
  - benefit tags  
  - disadvantage tags  
  - semantic similarity scores  
- Sources:  
  - **Sephora** (Bazaarvoice)  
  - **Ulta & Shoppers Drug Mart** (PowerReviews)

---

## ⚙️ Models Implemented

### Classical
- **TF-IDF + Logistic Regression**

### Transformer Models
- **BERT (bert-base-uncased)**  
- **BART**  
- **GPT-4o-mini** for high-quality benefit/disadvantage extraction  

### Keyword & Aspect Models
- **KeyBERT**  
- Early experiments with **VADER** and **Flan-T5**

### Similarity Modeling
- TF-IDF vectorization of extracted benefits  
- Cosine similarity matrix for product-to-product comparison  
- Heatmaps for moisturizer and foundation categories  

---

## 🌐 Streamlit App
The Streamlit application allows users to:
- Select **foundation** or **moisturizer**  
- View extracted **benefits** and **disadvantages**  
- See the **most similar product** based on NLP similarity  

Run locally:
```bash
streamlit run app.py


## 🧠 Next Steps

- Add additional product categories
- Improve similarity using SBERT
- Add product images and brand metadata
- Deploy the Streamlit app online
=======