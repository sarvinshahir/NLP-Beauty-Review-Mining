# Multi-Source Review Mining: Pros, Cons, and Product Similarity
**Author:** Sarvin Shahir

This project analyzes beauty product reviews collected from Sephora, Ulta, and Shoppers Drug Mart.  
Using NLP techniques, it extracts key **benefits**, **disadvantages**, and **similarity scores**, and provides an interactive Streamlit app for comparison.

---

## Overview

The goal of this project is to understand how beauty products compare based on real customer feedback.  
NLP methods were used to extract pros/cons, transform the reviews into numerical vectors, and compute how similar different products are to each other.

A Streamlit app allows users to:
- Select a product category  
- View product benefits and disadvantages  
- Find the most similar product based on TF-IDF similarity  

---

## Project Structure



data/
all_reviews.csv
all_reviews_foundation.csv
all_reviews_moisture.csv
nlp_merged_reviews.csv
products_benefit_disadv.csv
products_final.csv
similarity_matrix.csv

notebooks/
dataset1.ipynb
dataset_foundation.ipynb
dataset_moisturizer.ipynb
EDA.ipynb
TF_IDF.ipynb
BERT.ipynb
BART.ipynb
KeyBert.ipynb
GPT_4o_mini.ipynb
opinion_mining.ipynb
Comparison.ipynb
before_streamlit.ipynb

outputs/
heatmaps/
similarity_plots/
model_results/

app.py
requirements.txt
README.md


---

## Methods

### 1. Data Gathering
Reviews were merged from three platforms:
- Sephora  
- Ulta  
- Shoppers Drug Mart  

### 2. NLP Extraction
GPT-4o-mini was used to extract:
- Benefits  
- Disadvantages  

Saved in `products_benefit_disadv.csv`.

### 3. TF-IDF Similarity
Benefits were vectorized with TF-IDF, and cosine similarity was computed to create:
- `similarity_matrix.csv`  

This allows recommendation of the most similar product.

### 4. Streamlit App
The app lets users:
- Choose moisturizer/foundation  
- View extracted insights  
- Get the most similar product recommendation  

Run locally:

```bash
streamlit run app.py

Installation
pip install -r requirements.txt

Next Steps

Add more products

Improve similarity using SBERT

Add product images

Deploy the Streamlit app online

Acknowledgments

Reviews were collected from:

Sephora (Bazaarvoice)

Ulta & Shoppers Drug Mart (PowerReviews)

This project was part of Northeastern University’s IE 7500 NLP coursework.
