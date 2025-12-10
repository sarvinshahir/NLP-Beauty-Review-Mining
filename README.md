# Multi-Source Review Mining: Pros, Cons, and Product Similarity  
## Author: Sarvin Shahir  
### Northeastern University — IE 7500 Natural Language Processing

---

## 📌 Project Overview

This project analyzes customer reviews for beauty products collected from Sephora, Ulta, and Shoppers Drug Mart.  
Using NLP techniques and transformer-based models, the project extracts:

- **Benefits (pros)**  
- **Disadvantages (cons)**  
- **Product similarity scores**  
- **Brand-level comparison heatmaps**  

A **Streamlit application** is included to allow interactive product exploration and recommendation.

The goal is to build a reproducible NLP pipeline that transforms raw multi-source reviews into structured product insights.

---

## 📁 Repository Structure


### Root Files
- README.md  
- requirements.txt
- requirements2.txt
- app.py  

### Folders
- **data/** — raw and processed CSV files  
- **notebooks/** — Preprocessing, Modeling 


---

## 📥 Installation

### 1. Create a virtual environment (recommended)
python3 -m venv venv
source venv/bin/activate

shell
Copy code

### 2. Install dependencies
pip install -r requirements.txt


### 3. Python version
This project was developed with **Python 3.10+**.

---

## 📂 Data Preparation

### Data Sources  
Reviews were collected from:

- **Sephora** (Bazaarvoice API)  
- **Ulta & Shoppers Drug Mart** (PowerReviews API)

### Data Files Included  
- `all_reviews.csv` – merged foundation + moisturizer reviews  
- `all_reviews_foundation.csv`  
- `all_reviews_moisture.csv`  
- `nlp_merged_reviews.csv`  
- `products_benefit_disadv.csv` – GPT-extracted pros/cons  
- `products_final.csv` – includes manually assigned product category  
- `similarity_matrix.csv` – TF-IDF similarity results  

These files allow full reproduction of model results and the Streamlit app.

---

## 🔧 Running the Streamlit Application

Launch the interactive demo:
streamlit run app.py
requirements.txt


The app provides:
- Product category selection  
- Benefits & disadvantages extraction  
- Recommendation of most similar products  

All required CSVs are already included.

---

## 📓 Notebooks & Experiment Flow

| Notebook | Purpose |
|----------|---------|
| `1_dataset_collection.ipynb` | Collect/merge raw reviews from 3 retailers |
| `2_dataset_foundation.ipynb` | Clean + prepare foundation dataset |
| `3_dataset_moisturizer.ipynb` | Clean + prepare moisturizer dataset |
| `4_EDA.ipynb` | Visualization and preprocessing |
| `5_TF_IDF.ipynb` | Baseline ML model + feature extraction |
| `6_opinion_mining.ipynb` | T5 pros/cons extraction |
| `7_BERT.ipynb` | Transformer fine-tuning for review scoring |
| `8_BART.ipynb` | Summarization and aspect extraction |
| `9_KeyBert.ipynb` | Keyword-level benefit extraction |
| `10_GPT_4o_mini.ipynb` | High-quality pros/cons extraction |
| `11_Comparison.ipynb` | Cross-product comparison analysis |
| `12_before_streamlit.ipynb` | Generate files used by the Streamlit app |

All notebooks include explanations of methods, intermediate outputs, and decisions.

---

## 🧠 Models Implemented

### Classical
- **TF-IDF + Logistic Regression**

### Transformer Models
- **BERT (bert-base-uncased)**  
- **BART**
- **T5**    
- **GPT-4o-mini** (for pros/cons extraction)

### Keyword & Aspect Models
- **KeyBERT**  
- Experiments with **VADER** and **Flan-T5**

### Similarity Modeling
- TF-IDF vectorization over extracted benefits  
- Cosine similarity matrix  
- Heatmaps for foundations and moisturizers  

---

## 🔁 Reproducibility

### Random Seeds  
Where applicable:
np.random.seed(42)
torch.manual_seed(42)


### Computational Requirements  
- Any modern laptop CPU is sufficient  
- GPU optional for transformer fine-tuning (Google Colab recommended)

### How to Reproduce the Results  
1. Run the preprocessing notebooks (`1–3`)  
2. Run EDA + TF-IDF experiments (`4–5`)  
3. Run transformation models (`7–10`)  
4. Generate comparison + similarity results (`11–12`)  
5. Launch Streamlit for product exploration  
6. All required CSV outputs are included  

---

## 📈 Summary of Key Results

- GPT-4o-mini extracted the **most consistent** benefit/disadvantage lists  
- TF-IDF benefits produced clear brand similarity groupings  
- Foundations are most similar in pairs: **Armani ↔ Dior**, **Lancôme ↔ Estée Lauder**  
- Moisturizers showed higher cross-brand similarity patterns  
- Streamlit app enables fast product comparison  


---

## 👥 Team Members & Contributions
**Sarvin Shahir (Solo Project)**  
- Data collection & cleaning  
- Model development (TF-IDF, BERT, BART, GPT)  
- Pros/cons extraction  
- Heatmaps and similarity results  
- Streamlit application  
- Full documentation & reproducibility setup  

---

## 📚 Citations & External Resources

- HuggingFace Transformers  
- Scikit-Learn  
- KeyBERT  
- Streamlit  
- Bazaarvoice & PowerReviews APIs  
- OpenAI GPT models  

---

## 🧩 Requirements File

All software dependencies are listed in:

requirements2.txt