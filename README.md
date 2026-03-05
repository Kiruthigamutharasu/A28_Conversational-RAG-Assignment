# Conversational RAG Chatbot using LangChain + Ollama

##  Project Overview

This project implements a **Conversational Retrieval-Augmented Generation (RAG) Chatbot** using LangChain and locally running Ollama models.

The system allows users to ask questions about a document and supports **multi-turn conversations**, enabling follow-up questions that depend on previous context.

Unlike traditional chatbots, responses are generated strictly from retrieved document content, reducing hallucinations.

---

##  Objectives

- Load and process large PDF documents
- Create embeddings and store them in a vector database
- Retrieve relevant context using semantic search
- Build a conversational RAG pipeline
- Maintain chat history across turns
- Implement chat history trimming for efficiency

---

##  System Architecture

User Question  
→ Retriever (Chroma Vector DB)  
→ Context Retrieval  
→ Prompt + Chat History  
→ Local LLM (Ollama)  
→ Grounded Answer

---

##  Technologies Used

| Component | Tool / Model |
|---|---|
| Framework | LangChain |
| LLM | Ollama (`llama3.2:1b`) |
| Embeddings | Ollama (`nomic-embed-text`) |
| Vector Database | ChromaDB |
| Language | Python 3.11 |
| Document Loader | PyPDFLoader |

---

##  Project Structure
Conversational-RAG-Assignment/
│
├── rag_chatbot.ipynb # Main notebook (submission)
├── data/
│ └── ml_book.pdf # Source document
├── chroma_db/ # Vector database (auto-created)
├── requirements.txt
└── README.md

book pdf used is : 
Mathematics for Machine Learning (Open Educational Resource)
https://mml-book.github.io/book/mml-book.pdf
---

##  Setup Instructions

### 1️⃣ Create Virtual Environment

```bash
py -3.11 -m venv venv
venv\Scripts\activate

2️⃣ Install Dependencies
pip install -r requirements.txt


 3. Install & Run Ollama
Download: https://ollama.com

Pull models:
ollama pull nomic-embed-text
ollama pull llama3.2:1b

Open `rag_chatbot.ipynb` and select Python 3.11 kernel.

---

## 💬 Features
- Document-based question answering
- Semantic search using embeddings
- Conversational memory
- Follow-up question handling
- Chat history trimming



