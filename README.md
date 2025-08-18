# 🧠 Comparative QA System: RAG vs Fine-Tuning

This repository implements a dual-mode Question Answering system on financial documents using:

1. **Retrieval-Augmented Generation (RAG)** with hybrid retrieval (Dense + BM25) and Cross-Encoder Re-ranking.
2. **Fine-Tuned Language Model** on custom Q/A pairs from annual reports.

---

## 🔧 Project Structure

| Folder         | Description |
|----------------|-------------|
| `data/`        | Raw financial files, cleaned text, Q/A dataset |
| `embeddings/`  | FAISS & BM25 index, metadata |
| `fine_tuned_model/` | Fine-tuned model artifacts |
| `app/`         | Streamlit/Gradio app UI |
| `evaluation/`  | Comparison results, test logs |
| `report/`      | Final report with screenshots |
| `notebooks/`   | Main RAG + FT implementation |
| `utils/`       | Reusable code modules |

---

## 🚀 How to Run

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Launch UI
```bash
streamlit run app/app.py
```

---

## 📚 Methods Used

### 🧠 RAG
- FAISS + BM25 hybrid retrieval
- Cross-Encoder re-ranking
- DistilGPT2 for generation

### 🎯 Fine-Tuning
- Fine-tuned `DistilBERT` on 50 Q/A pairs
- Mixture-of-Experts architecture

---

## 📈 Evaluation

- Tested on:
  - High/Low confidence queries
  - Irrelevant queries
- Metrics:
  - Answer accuracy
  - Confidence score
  - Inference time

---

## 🛡️ Guardrails

- Input sanitization
- Output factuality check for hallucinations

---

## 📌 Authors

- Group 4 — BITS Pilani MTech AI/ML

---

## 📎 License

MIT License
