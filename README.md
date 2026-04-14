# 🔑 Section-Aware Keyphrase Extraction using SciBERT

This project builds a keyphrase extraction system for scientific text using **SciBERT** and **BIO tagging**. It improves performance by making the model aware of document structure (Title + Abstract).

---

## 🚀 Features

* Fine-tuned SciBERT for scientific text
* BIO tagging (B-KEY, I-KEY, O)
* Section-aware input: `[TITLE] + [ABSTRACT]`
* Token classification approach
* TF-IDF baseline comparison
* Evaluation using Precision, Recall, F1-score

---

## 🧠 Approach

* Combine title and abstract with special tokens
* Generate BIO labels from keyphrases
* Tokenize using SciBERT tokenizer
* Fine-tune model for token classification
* Reconstruct keyphrases from predictions

---

## 📊 Dataset

KP20K dataset (scientific papers):

* 530K training samples
* 20K validation, 20K test

https://huggingface.co/datasets/midas/kp20k

---

## 📈 Results

* TF-IDF F1-score: 0.09
* SciBERT F1-score: 0.40 ✅

---

## 📌 Example

Input:
Title: Federated Learning for Privacy Preserving Medical AI
Abstract: This proposal introduces a decentralized learning framework...

Output:
["federated learning", "privacy preserving", "medical ai"]

---

## 🛠️ Tech Stack

Python, PyTorch, Hugging Face, SciBERT, scikit-learn, NumPy, Pandas

