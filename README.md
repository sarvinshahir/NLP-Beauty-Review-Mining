# Multi-Source Review Mining: Pros, Cons, and Product Similarity  
**Author:** Sarvin Shahir  

This project analyzes beauty product reviews collected from Sephora, Ulta, and Shoppers Drug Mart.  
Using NLP techniques, the project extracts **benefits**, **disadvantages**, and **cross-product similarities**, and provides an interactive Streamlit app for easy exploration.

---

## 📁 Project Structure

project/
│ README.md
│ requirements.txt
│ app.py
│
├── data/
│ ├── all_reviews.csv
│ ├── all_reviews_foundation.csv
│ ├── all_reviews_moisture.csv
│ ├── nlp_merged_reviews.csv
│ ├── products_benefit_disadv.csv
│ ├── products_final.csv
│ └── similarity_matrix.csv
│
├── notebooks/
│ ├── dataset1.ipynb
│ ├── dataset_foundation.ipynb
│ ├── dataset_moisturizer.ipynb
│ ├── EDA.ipynb
│ ├── TF_IDF.ipynb
│ ├── BERT.ipynb
│ ├── BART.ipynb
│ ├── KeyBert.ipynb
│ ├── GPT_4o_mini.ipynb
│ ├── opinion_mining.ipynb
│ ├── Comparison.ipynb
│ └── before_streamlit.ipynb
│
└── outputs/
├── heatmaps/
├── similarity_plots/
└── model_results/

yaml
Copy code

---

## 🧪 NLP Tasks Completed

### **1. Data Collection**
Reviews were extracted from:
- Sephora (Bazaarvoice)
- Ulta & Shoppers Drug Mart (PowerReviews)

Files:
- `all_reviews.csv`
- `all_reviews_foundation.csv`
- `all_reviews_moisture.csv`
- `nlp_merged_reviews.csv`

---

### **2. Benefit & Disadvantage Extraction**
Using **GPT-4o-mini**, each product was assigned:
- a list of **benefits**  
- a list of **disadvantages**

Stored in:
- `products_benefit_disadv.csv`

---

### **3. Product Categorization**
Each product was manually labeled as:
- *foundation*  
- *moisturizer*

Stored in:
- `products_final.csv`

---

### **4. Similarity Analysis**
Using TF-IDF + cosine similarity:
- Benefits were vectorized  
- Product-to-product similarity matrix was computed  
- Visual heatmaps were produced

Stored in:
- `similarity_matrix.csv`

---

### **5. Model Experiments**
This project includes experiments with:
- **TF-IDF + Logistic Regression**
- **BERT (bert-base-uncased)**
- **BART**
- **KeyBERT**
- **GPT-4o-mini**
- Comparison of pros/cons extraction performance

All steps documented inside notebooks.

---

## 🌐 Streamlit Application

An interactive app that allows users to:

- View **product benefits** and **disadvantages**
- Filter by **foundation** or **moisturizer**
- Find the **most similar product** based on extracted benefits

Run locally:

```bash
streamlit run app.py
🧠 Next Steps
Add more beauty products

Use SBERT for stronger semantic similarity

Add product images and brand metadata

Deploy Streamlit app online

📦 Installation
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Launch Jupyter notebooks:
jupyter notebook

🤝 Acknowledgments
Customer reviews were sourced from:

Sephora (Bazaarvoice API)

Ulta & Shoppers Drug Mart (PowerReviews API)

This project was completed as part of Northeastern University’s NLP course (IE 7500).

