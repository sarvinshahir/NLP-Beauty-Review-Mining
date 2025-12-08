Multi-Source Review Mining: Pros, Cons, and Product Similarity
Author: Sarvin Shahir

This project analyzes beauty product reviews collected from Sephora, Ulta, and Shoppers Drug Mart. 
It extracts benefits, disadvantages, and product similarity using NLP methods, and includes a Streamlit app for interactive comparison.

---

Project Structure

### Data
- all_reviews.csv  
- all_reviews_foundation.csv  
- all_reviews_moisture.csv  
- nlp_merged_reviews.csv  
- products_benefit_disadv.csv  
- products_final.csv  
- similarity_matrix.csv  

### Notebooks
- dataset1.ipynb  
- dataset_foundation.ipynb  
- dataset_moisturizer.ipynb  
- EDA.ipynb  
- TF_IDF.ipynb  
- BERT.ipynb  
- BART.ipynb  
- KeyBert.ipynb  
- GPT_4o_mini.ipynb  
- opinion_mining.ipynb  
- Comparison.ipynb  
- before_streamlit.ipynb  

### Outputs
- heatmaps/  
- similarity_plots/  
- model_results/  

### Other Files
- app.py  
- requirements.txt  
- README.md  

---

Methods

### 1. Data Collection
Reviews were collected from Sephora, Ulta, and Shoppers Drug Mart.  
All merged into CSV files inside the data/ folder.

### 2. NLP Extraction
GPT-4o-mini was used to extract product benefits and disadvantages.  
Saved in products_benefit_disadv.csv.

### 3. Model Experiments
The project includes experiments using:
- TF-IDF + Logistic Regression  
- BERT (bert-base-uncased)  
- BART  
- KeyBERT  
- GPT-4o-mini  
All experiments are documented in the notebooks.

### 4. Similarity Computation
- TF-IDF applied to extracted benefits  
- Cosine similarity computed for product-to-product comparison  
- Heatmaps and similarity plots generated  
Matrix saved in similarity_matrix.csv.

### 5. Streamlit App
The app supports:
- Selecting moisturizer or foundation  
- Viewing extracted benefits/disadvantages  
- Recommending the most similar product  

Run:
streamlit run app.py

---

Installation
pip install -r requirements.txt

---

Next Steps
- Add more products  
- Improve similarity with SBERT  
- Add product images  
- Deploy the Streamlit app online  

---

Acknowledgments
Reviews collected from:
- Sephora (Bazaarvoice)  
- Ulta (PowerReviews)  
- Shoppers Drug Mart (PowerReviews)  

This project was completed for Northeastern University’s IE 7500 NLP course.
<img width="468" height="638" alt="image" src="https://github.com/user-attachments/assets/d78b61a1-0399-451c-a970-3560b7914043" />
