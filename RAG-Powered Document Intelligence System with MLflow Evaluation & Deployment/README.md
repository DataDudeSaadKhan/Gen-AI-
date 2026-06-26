
***

````markdown
<div align="center">
  <h1>
    🧠 RAG-Based Intelligent Document Q&A System (Azure Deployment)
  </h1>
</div>

<p align="center">
  img.shields.io/badge/AI-Retrieval--Augmented%20Generation-blue?style=flat-square"/>
  /Embeddings-ChromaDB%20Vector%20Search-lightblue?style=flat-square"/>
  <img src="https://img.shields.io/badge/LLM-Anthropic%20Claude-purple?style=flat-square"/>
  <img src="https://img.shields.io/badge/Evaluation-MLflow-orange?style=flat-square"/>
  <img src=https://img.shields.io/badge/Deployment-Azure%20Cloud-0078D4?style=flat-square
  img.shields.io/badge/Container-Docker-2496ED?style=flat-square"/>
  <img src="https://img.shields.io/badge/UI-Streamlit-red?style=flat-square"/>
</p>

---

# 🧠 Overview

This project delivers a **production-grade Retrieval-Augmented Generation (RAG) system** that enables users to query **private document corpora** and receive **accurate, context-aware, source-grounded answers**.

Deployed on **Microsoft Azure**, the system is designed for **real-world client delivery as a freelancer solution**.

---

# 🧠 Business Problem

Professionals working with large document collections struggle to:

- Extract precise answers quickly  
- Navigate unstructured PDFs  
- Use traditional keyword search effectively  

➡️ This leads to **inefficiency and missed insights**

---

# 🎯 Solution

A **RAG pipeline** that:

✅ Understands natural language queries  
✅ Retrieves relevant document chunks  
✅ Generates accurate answers using LLM  
✅ Provides **traceable citations**

---

# ⚙️ Architecture Diagram

## 🔹 Visual (Mermaid)

```mermaid
flowchart TD
    A[User Query - Streamlit UI] --> B[Retriever Layer]
    B --> C[ChromaDB Vector Store]
    C --> D[Top-K Relevant Chunks]
    D --> E[Prompt Augmentation]
    E --> F[Anthropic Claude LLM]
    F --> G[Answer + Sources]
    G --> A
````

***

## 🔹 Simplified Flow

```
User → Web App (Streamlit)
     → Vector Search (ChromaDB)
     → Context Retrieval
     → LLM (Claude API)
     → Answer + Sources
```

***

# 📊 Data & Inputs

* 15 Oncology PDFs
* Natural language queries
* Embeddings:
  * all-MiniLM-L6-v2
* Vector DB:
  * ChromaDB (cosine similarity)

***

# 🔧 Technical Components

### 1. Ingestion

* PyPDFLoader (LangChain)

### 2. Chunking

* Recursive splitting with overlap

### 3. Embeddings

* Sentence Transformers

### 4. Retrieval

* Top-K + similarity filtering

### 5. LLM

* Anthropic Claude API

### 6. Evaluation

* 216 MLflow experiments
* Metrics:
  * Hit Rate\@K
  * Precision\@K
  * Recall\@K

***

# ☁️ Azure Deployment

## 🔹 Services Used

* Azure App Service / Container Apps
* Azure Container Registry (ACR)
* Azure Storage (Vector DB persistence)
* Azure Key Vault (Secrets)
* Azure Monitor

***

## 🔹 Deployment Flow

```
Local → Docker Build → ACR → Azure App Service → Live Web App
```

***

# 🌐 Live Demo

```
https://rag-doc-assistant.azurewebsites.net
```

### Demo Capabilities:

* Ask medical questions
* Get instant contextual answers
* View supporting document sources

***

# 🐳 Docker

```bash
docker build -t rag-qa-system .
docker run -p 8501:8501 rag-qa-system
```

***

# 🛠 Tech Stack

| Layer      | Tools                 |
| ---------- | --------------------- |
| UI         | Streamlit             |
| Backend    | Python, LangChain     |
| Embeddings | Sentence Transformers |
| Vector DB  | ChromaDB              |
| LLM        | Claude API            |
| Tracking   | MLflow                |
| Cloud      | Azure                 |
| Container  | Docker                |

***

# 🚀 Key Achievements

* End-to-end RAG system built
* Optimized via MLflow experimentation
* Azure production deployment
* Low-latency retrieval system
* Client-ready private document assistant

***

# 💼 Freelance Use Case

Customizable for:

* Healthcare
* Legal
* Research
* Enterprise knowledge systems

***

# 📬 Contact

**Mohammad Saad**  
Data Scientist | Data Engineer

Available for:

* RAG system development
* Azure AI deployments
* Private document intelligence solutions

***

# ⭐ Future Enhancements

* Hybrid search
* Multi-language support
* Enterprise integrations

```