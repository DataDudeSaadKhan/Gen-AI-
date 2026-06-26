<div align="center">
  <h1>
    🧠 RAG-Based Intelligent Document Q&A System (Azure Deployment)
  </h1>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/AI-Retrieval--Augmented%20Generation-blue?style=flat-square"/>
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

Professionals working with large volumes of unstructured documents struggle to:

- Extract precise answers quickly  
- Navigate large PDF corpora efficiently  
- Use traditional keyword search effectively  

➡️ This results in **lost productivity and inefficient decision-making**

---

# 🎯 Solution

A **Retrieval-Augmented Generation (RAG) system** that:

✅ Understands natural language queries  
✅ Retrieves semantically relevant chunks  
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

***

## 🔹 System Flow (Readable)

```
User → Streamlit UI → Retriever → Vector DB → Context Chunks
     → Prompt Builder → Claude LLM → Answer + Sources
```

***

# 📊 Data & Inputs

* 15 domain-specific oncology PDF documents
* Natural language user queries
* Embeddings model:
  * `all-MiniLM-L6-v2` (Sentence Transformers)
* Vector database:
  * ChromaDB with cosine similarity

***

# 🔧 Technical Implementation

## 1️⃣ Document Ingestion

* Parsed PDFs using **LangChain PyPDFLoader**

## 2️⃣ Text Chunking

* Recursive splitting with configurable:
  * Chunk size
  * Overlap

## 3️⃣ Embeddings

* Generated via **Sentence Transformers**

## 4️⃣ Vector Storage

* Stored in **ChromaDB**
* Persistent and preloaded for low latency

## 5️⃣ Retrieval Pipeline

* Top-K retrieval
* Similarity threshold filtering

## 6️⃣ LLM Integration

* Powered by **Anthropic Claude API**
* Supports multi-turn conversations
* Context-aware answers

***

# 📈 Evaluation Framework

* 20 ground-truth Q\&A pairs
* Metrics:
  * Hit Rate\@K
  * Precision\@K
  * Recall\@K

📊 Conducted:

* **216 MLflow experiments**

➡️ Optimized:

* Chunk size
* Overlap
* Retrieval parameters
* Embedding configurations

***

# ☁️ Azure Deployment

## 🔹 Services Used

* Azure App Service / Container Apps
* Azure Container Registry (ACR)
* Azure Storage (Vector DB persistence)
* Azure Key Vault (API security)
* Azure Monitor (logging)

***

## 🔹 Deployment Workflow

```
Local Development
   ↓
Docker Containerization
   ↓
Push to Azure Container Registry
   ↓
Deploy to Azure App Service
   ↓
Live Web Application
```

***

# 🌐 Live Demo

```
https://rag-doc-assistant.azurewebsites.net
```

### Demo Capabilities:

* Ask domain-specific questions
* Receive instant contextual answers
* View supporting document sources

***

# 🖥 User Interface

Built using **Streamlit**:

* Chat-based interface
* Dark mode UI
* Real-time responses
* Expandable context sources

***

# 🐳 Docker Setup

```bash
docker build -t rag-qa-system .
docker run -p 8501:8501 rag-qa-system
```

***

# 🔐 Security & Privacy

✅ Designed for private datasets  
✅ Secure API key management via Azure Key Vault  
✅ No external data leakage  
✅ Suitable for sensitive domains

***

# 📈 Scalability

* Azure-based horizontal scaling
* Supports multi-user scenarios
* Extendable to SaaS architecture

***

# 🛠 Tech Stack

| Layer               | Technology            |
| ------------------- | --------------------- |
| UI                  | Streamlit             |
| Backend             | Python, LangChain     |
| Embeddings          | Sentence Transformers |
| Vector DB           | ChromaDB              |
| LLM                 | Anthropic Claude      |
| Experiment Tracking | MLflow                |
| Containerization    | Docker                |
| Cloud               | Microsoft Azure       |

***

# 🚀 Key Achievements

* ✅ End-to-end RAG system development
* ✅ High retrieval accuracy via tuning
* ✅ Production deployment on Azure
* ✅ Low-latency response system
* ✅ Modular and scalable pipeline design

***

# 💼 Freelance Use Case

This solution can be adapted for:

* 🏥 Healthcare document intelligence
* ⚖️ Legal contract analysis
* 📊 Business research tools
* 📚 Educational assistants

***

# 📬 Contact

**Saad Khan**  
Data Scientist and Engineer

Available for:

* RAG system development
* Azure AI deployments
* Document intelligence solutions

***

# ⭐ Future Enhancements

* Hybrid search (BM25 + Vector)
* Multilingual support
* Feedback-driven ranking
* Enterprise integrations

```
