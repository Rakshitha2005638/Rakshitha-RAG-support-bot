# 🤖 RAG-Based Customer Support Assistant (LangGraph + HITL)

## 📌 Project Overview

This project is a **Retrieval-Augmented Generation (RAG) based Customer Support Assistant** that answers user queries using a PDF knowledge base.

The system retrieves relevant information from documents and generates accurate responses using a Large Language Model (LLM). It also supports **Human-in-the-Loop (HITL)** escalation for low-confidence queries.

---

## 🚀 Features

* PDF-based knowledge retrieval
* Context-aware answer generation
* LangGraph workflow orchestration
* Conditional routing based on confidence
* Human-in-the-Loop (HITL) escalation
* Fast retrieval using ChromaDB

---

## 🏗️ System Architecture

User → Query → LangGraph → Retriever → ChromaDB
↓
LLM
↓
Answer / HITL

---

## 📂 Project Structure

rag-support-bot/
│
├── data/
│   └── support.pdf
│
├── src/
│   ├── main.py
│   ├── ingest.py
│   ├── embedder.py
│   ├── retriever.py
│   ├── llm.py
│   ├── graph.py
│   └── hitl.py
│
├── db/
├── requirements.txt
├── .env
└── documents/
│   ├── HLD
│   ├──LLD
│   ├── Technical document

---

## ⚙️ Installation & Setup

### 1. Clone Repository

git clone <your-repo-link>
cd rag-support-bot

---

### 2. Create Virtual Environment

python -m venv venv
venv\Scripts\activate

---

### 3. Install Dependencies

pip install -r requirements.txt

---

### 4. Setup Environment Variables

Create a `.env` file:

OPENAI_API_KEY=your_api_key_here

---

### 5. Add PDF

Place your support document inside:

data/support.pdf

---

### 6. Run Project

python -m src.main

---

## 🧠 How It Works

1. PDF is loaded and split into chunks
2. Chunks are converted into embeddings
3. Stored in ChromaDB
4. User query is processed
5. Relevant chunks are retrieved
6. LLM generates response
7. System routes output:

   * Answer → if confident
   * HITL → if low confidence

---

## 🔀 LangGraph Workflow

* Input Node
* Retrieval Node
* Generation Node
* Routing Node
* HITL Node

---

## 🧑‍💼 Human-in-the-Loop (HITL)

If the system has low confidence:

* Query is escalated to a human
* Human provides response
* Response is returned to user

---

## 🧪 Testing

Example queries:

* How do I reset my Microsoft account password?
* What should I do if I forgot my password?
* Random question (triggers HITL)

---

## ⚠️ Challenges

* Retrieval accuracy vs speed
* API latency
* Chunk size optimization

---

## 🚀 Future Improvements

* Streamlit UI
* Multi-document support
* Chat memory
* Feedback loop

---

## 🛠️ Technologies Used

* Python
* LangChain
* LangGraph
* ChromaDB
* HuggingFace Embeddings
* OpenAI

---

## 📌 Conclusion

This project demonstrates how RAG systems can be used to build scalable and intelligent customer support assistants with decision-making capabilities and human fallback.

---

## 🙌 Acknowledgement

This project was developed as part of a GenAI internship program.

---

## 🎥 Demo Video

https://drive.google.com/file/d/1AYEoQGCdQsdfg7cmkkGnBlY5oWkBBuLf/view?usp=vids_web
