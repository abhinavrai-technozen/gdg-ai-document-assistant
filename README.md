# AI-Powered Document Assistant (GDG-USAR Project)

An end-to-end Retrieval-Augmented Generation (RAG) pipeline built for querying specific document passages with source attribution and strict answer grounding.

## 📌 Project Overview
This tool converts PDF/TXT documents into searchable vector embeddings, retrieves relevant document passages based on user queries, and uses an open-source LLM to generate grounded answers with page citations.

## 🛠️ Features
- **Document Chunking & Storage:** Splits document content into structured passages using LangChain and indexes them using Chroma Vector DB.
- **Strict Grounding:** Prevents model hallucinations by enforcing the model to answer *only* from the provided document context.
- **Source Attribution:** Returns exact source page numbers and text snippets used for generating answers.
- **Refusal on Out-of-Scope Queries:** Safely handles queries unanswerable from the document text.

## 🧪 Experiments (`DECISIONS.md`)
Tested two chunking configurations:
- **Experiment 1:** Chunk size 1000, overlap 100 (\(k=2\)).
- **Experiment 2 (Optimal):** Chunk size 500, overlap 50 (\(k=3\)). Evaluated to provide higher precision and better page attribution.

## 🚀 How to Run
1. Open `Copy_of_Untitled1.ipynb` in Google Colab.
2. Execute Cell 1 to install dependencies.
3. Run Cell 2 to upload your PDF/TXT document.
4. Execute Cells 3 & 4 to build the RAG pipeline and run evaluation queries.
