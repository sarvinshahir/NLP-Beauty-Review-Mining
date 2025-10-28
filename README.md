# Multi-Source Review Mining: Pros, Cons, and Comparison of Beauty Products
**Author:** Sarvin Shahir  

This project analyzes beauty product reviews from multiple retailers — Sephora, Ulta, and Shoppers Drug Mart — using Natural Language Processing (NLP) techniques to extract sentiment, pros, and cons.

---

## 📁 Project Structure
data/ → Contains the raw and cleaned CSV datasets
notebooks/ → Jupyter notebooks for each stage
outputs/ → Evaluation results and visuals

yaml
Copy code

| Notebook | Purpose |
|-----------|----------|
| `dataset1.ipynb` | API extraction for 4 products from 3 retailers |
| `EDA.ipynb` | Cleaning, preprocessing, and exploratory visualizations |
| `TF_IDF.ipynb` | Baseline sentiment model |
| `BERT.ipynb` | Transformer fine-tuning for rating prediction |
| `opinion_mining.ipynb` | Pros and cons extraction experiments |

---

## 📊 Dataset
- 4 foundation products: NARS, Estée Lauder, Dior, Armani  
- 200–300 reviews per product (≈ 1 000 total)  
- Sources: Sephora (Bazaarvoice), Ulta & Shoppers (PowerReviews)

---

## ⚙️ Models Implemented
1. **TF-IDF + Logistic Regression**  
2. **BERT (bert-base-uncased)**  
3. **Aspect extraction prototypes** (VADER & Flan-T5)

---

## 🧠 Next Steps
- Add more products  
- Implement RNN (LSTM)  
- Improve pros/cons extraction  
- Build Streamlit app for interactive comparison

---

## 🚀 How to Run
```bash
pip install -r requirements.txt
jupyter notebook notebooks/