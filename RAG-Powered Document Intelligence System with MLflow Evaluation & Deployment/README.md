<div align="center">
  <h1>
    🧠 RAG-Based Intelligent Document Q&A System (Azure Deployment)
  </h1>
</div>

<p align="center">
  AI-Retrieval--Augmented%20Generation-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Embeddings-ChromaDB%20Vector%20Search-lightblue?style=flat-square"/>
  <img src="https://img.shields.io/badge/LLM-Anthropic%20Claude-purple?style=flat-square"/>
  <img src="https://img.shields.io/badge/Evaluation-MLflow-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Deployment-Azure%20Cloud-0078D4?style=flat-square"/>
  <img src="https://img.shields.io/badge/Container-Docker-2496ED?style=flat-square"/>
  <img src="https://img.shields.io/badge/UI-Streamlit-red?style=flat-square"/>
</p>

---

# 📌 Overview

This project delivers a **production-grade Retrieval-Augmented Generation (RAG) system** that enables users to query **private document corpora** and receive **accurate, context-aware, source-grounded answers**.

Deployed on **Microsoft Azure Cloud**, the system is designed for **real-world client delivery as a freelancer solution**.

---

# 🧠 Business Problem

Professionals working with large volumes of unstructured documents (medical, legal, research) struggle to:

- Extract precise answers quickly  
- Navigate large PDF corpora efficiently  
- Use traditional keyword search effectively  

➡️ This results in **lost productivity and inefficient decision-making**.

---

# 🎯 Solution

A **Retrieval-Augmented Generation (RAG) system** that:

✅ Understands natural language queries  
✅ Retrieves semantically relevant document chunks  
✅ Generates accurate answers using LLMs  
✅ Provides **source-backed responses**

---

# ⚙️ Architecture Diagram

## 🔹 Visual

```mermaid
flowchart LR
    A[User] --> B[Streamlit Web App]
    B --> C[Retriever Layer]
    C --> D[(ChromaDB Vector Store)]
    D --> E[Top-K Relevant Chunks]
    E --> F[Prompt Augmentation]
    F --> G[Claude LLM API]
    G --> H[Answer + Source Citations]
    H --> B
````

***

## 🔹 System Flow

```
User → Streamlit UI → Retriever → Vector DB → Context Chunks
     → Prompt Builder → Claude LLM → Answer + Sources
```

***

# 📊 Data & Inputs

* 15 domain-specific oncology PDF documents
* Natural language user queries
* Embedding model: `all-MiniLM-L6-v2`
* Vector DB: ChromaDB

***

# 🔧 Technical Implementation

## 1️⃣ Document Ingestion

* Parsed PDFs using **LangChain PyPDFLoader**

## 2️⃣ Text Chunking

* Recursive splitting with overlap

## 3️⃣ Embeddings

* Generated via **Sentence Transformers**

## 4️⃣ Vector Storage

* Stored in **ChromaDB**
* Persistent and preloaded

## 5️⃣ Retrieval Pipeline

* Top-K retrieval
* Similarity filtering

## 6️⃣ LLM Integration

* **Anthropic Claude API**
* Multi-turn conversations
* Context-aware responses

***

# 📈 Evaluation Framework

* 20 Q\&A pairs
* Metrics:
  * Hit Rate\@K
  * Precision\@K
  * Recall\@K

✅ 216 MLflow experiments

***

# ☁️ Azure Deployment

### Services Used

* Azure App Service / Container Apps
* Azure Container Registry (ACR)
* Azure Storage
* Azure Key Vault
* Azure Monitor

### Deployment Flow

```
Local → Docker → ACR → Azure → Live App
```

***

# 🌐 Live Demo

```
https://rag-doc-assistant.azurewebsites.net
```

***

# 🖥 User Interface

* Streamlit chat UI
* Real-time responses
* Source citations display

***

# 🐳 Docker Setup

```bash
docker build -t rag-qa-system .
docker run -p 8501:8501 rag-qa-system
```

***

# 🔐 Security & Privacy

✅ Private dataset ready  
✅ Azure Key Vault for secrets  
✅ No external data leakage

***

# 📈 Scalability

* Azure horizontal scaling
* Multi-user support
* SaaS-ready architecture

***

# 🛠 Tech Stack

| Layer      | Technology            |
| ---------- | --------------------- |
| UI         | Streamlit             |
| Backend    | Python, LangChain     |
| Embeddings | Sentence Transformers |
| Vector DB  | ChromaDB              |
| LLM        | Anthropic Claude      |
| Tracking   | MLflow                |
| Container  | Docker                |
| Cloud      | Azure                 |

***

# 🚀 Key Achievements

* ✅ Built end-to-end RAG system
* ✅ Optimized via MLflow experiments
* ✅ Production Azure deployment
* ✅ Low-latency responses

***

# 💼 Freelance Use Case

* Healthcare
* Legal
* Research
* Enterprise knowledge systems

***

# 📬 Contact

**Mohammad Saad**  
Data Scientist & Engineer

***

# ⭐ Future Enhancements

* Hybrid search
* Multilingual support
* Feedback learning
* Enterprise integrations

```
