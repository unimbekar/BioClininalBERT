# 🧠 Biomedical Multi-label Classification using Bio_ClinicalBERT

This project fine-tunes [Bio_ClinicalBERT](https://huggingface.co/emilyalsentzer/Bio_ClinicalBERT) to perform multi-label classification on unstructured clinical notes using weak labels generated from a zero-shot NLP pipeline.

---

## 🔍 Use Case

Automatically assign clinical condition tags (e.g., `diabetes`, `cancer`, `mental_health`) to patient notes such as:
- Admission summaries
- Physician notes
- Intake questionnaires

This is useful for downstream tasks like:
- Case triaging
- High-risk flagging
- Patient summarization

---

## 🧪 Workflow Overview

1. **Zero-Shot Labeling with BART-MNLI**
   - Uses `facebook/bart-large-mnli` to weakly label clinical notes based on a predefined list of medical conditions.

2. **Fine-Tuning Bio_ClinicalBERT**
   - Trains `Bio_ClinicalBERT` with multi-label classification using the generated labels.

3. **Evaluation**
   - Model performance evaluated using Micro/Macro F1, Precision, and Recall.

---

## 📦 Requirements

- Python 3.7+
- Transformers
- Datasets
- Scikit-learn
- sentence-transformers
- PyTorch

Install dependencies:
```bash
pip install -q transformers datasets scikit-learn sentence-transformers
