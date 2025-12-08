# Multi-Source Review Mining: Pros, Cons, and Product Similarity
**Author:** Sarvin Shahir

This project analyzes beauty product reviews collected from Sephora, Ulta, and Shoppers Drug Mart.  
It extracts benefits, disadvantages, and product similarity using NLP methods, and includes a Streamlit app for interactive comparison.

---

## Project Structure

data/  
• all_reviews.csv  
• all_reviews_foundation.csv  
• all_reviews_moisture.csv  
• nlp_merged_reviews.csv  
• products_benefit_disadv.csv  
• products_final.csv  
• similarity_matrix.csv  

notebooks/  
• dataset1.ipynb  
• dataset_foundation.ipynb  
• dataset_moisturizer.ipynb  
• EDA.ipynb  
• TF_IDF.ipynb  
• BERT.ipynb  
• BART.ipynb  
• KeyBert.ipynb  
• GPT_4o_mini.ipynb  
• opinion_mining.ipynb  
• Comparison.ipynb  
• before_streamlit.ipynb  

outputs/  
• heatmaps/  
• similarity_plots/  
• model_results/  

Other files:  
• app.py  
• requirements.txt  
• README.md  

---

## Methods

### 1. Data Collection
Reviews were collected from 3 major platforms (Sephora, Ulta, Shoppers).  
All merged into CSV files inside the `data/` folder.

### 2. NLP Extraction
GPT-4o-mini was used to extract:  
• product benefits  
• disadvantages  

Stored in `products_benefit_disadv.csv`.

### 3. Similarity Computation
• TF-IDF applied to extracted benefits  
• Cosine similarity used to produce a product similarity matrix  
• Heatmaps and comparison plots generated  

Matrix saved in:  
`similarity_matrix.csv`

### 4. Streamlit App
The app supports:  
• selecting moisturizer or foundation  
• viewing extracted benefits/disadvantages  
• recommending the most similar product  

Run:

streamlit run app.py

yaml
Copy code

---

## Installation

pip install -r requirements.txt

yaml
Copy code

---

## Next Steps

• Add more products  
• Improve similarity with SBERT  
• Add product images  
• Deploy Streamlit app online  

---

## Acknowledgments

Reviews collected from:  
• Sephora (Bazaarvoice)  
• Ulta & Shoppers Drug Mart (PowerReviews)

This project was completed for Northeastern University’s IE 7500 NLP course.
