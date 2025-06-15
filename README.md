# 🧬 Biomedical Q&A Assistant with RAG, BioBERT, and Mistral
This project is an end-to-end Retrieval-Augmented Generation (RAG) pipeline designed to answer biomedical questions using your own dataset of research abstracts (e.g. PubMed articles). It combines:

* 🔍 Semantic search over custom documents (FAISS + Sentence Transformers)

* 🧠 Biomedical QA with a fine-tuned BioBERT model

* 🗣️ Natural rephrasing of answers using Mistral-7B Instruct

## 📌 Business Question
"Can we build a lightweight biomedical question-answering tool that provides both accurate and patient-friendly answers based on a custom research dataset?"

## 🛠️ Workflow Summary
* Custom Dataset: Upload your own CSV with PubMed-style fields (title, abstract, authors).

* Embedding: Generate document embeddings with all-MiniLM-L6-v2.

* FAISS Indexing: Perform fast nearest-neighbor retrieval for relevant documents.

* QA Inference: Use BioBERT to extract precise answers from top-retrieved documents.

* Answer Rephrasing: Rephrase technical responses into human-friendly language with Mistral.

## 🧪 Example Use Case
**Input**: “What treatments are recommended for PCOS?” <br> 
**Output**: <br> 

BioBERT: “Combined oral contraceptives, metformin, and lifestyle changes.”

Rephrased: “Doctors often recommend birth control pills, medications like metformin, and healthy habits like exercise and diet to manage PCOS.”

## ⚙️ Stack
* transformers, sentence-transformers, faiss-cpu, pandas, torch

* BioBERT: ktrapeznikov/biobert_v1.1_pubmed_squad_v2

* Mistral (gated): mistralai/Mistral-7B-Instruct-v0.2

## 🚧 Coming Soon
* Add a Streamlit front-end for user interaction

* Support for multi-turn question chains

* Explanation system (e.g. SHAP or attention visualization)

