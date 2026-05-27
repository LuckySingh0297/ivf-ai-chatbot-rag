# 🧬 IVF AI Chatbot (RAG-Based Healthcare Assistant)

> AI-powered IVF healthcare chatbot using RAG, FAISS, LangChain, SentenceTransformers, Ollama, and Streamlit for document-grounded medical question answering.

---

# 📌 Project Overview

The **IVF AI Chatbot** is a Retrieval-Augmented Generation (RAG) based healthcare assistant designed to provide accurate, context-aware, and document-grounded responses for IVF-related questions.

The system combines:
- Semantic Search
- Vector Databases
- Local LLM Inference
- Medical Knowledge Retrieval
- Healthcare Safety Guardrails

to create a reliable IVF patient support assistant.

---

# 🚨 Problem Statement

Patients undergoing IVF treatment often:
- struggle to understand complex medical terminology
- face anxiety due to lack of instant support
- search unreliable internet sources
- receive inconsistent information
- need 24/7 assistance outside clinic hours

Traditional chatbots hallucinate and provide generic responses.

This project solves that problem using **Retrieval-Augmented Generation (RAG)** to generate responses strictly from verified IVF medical documents.

---

# 💡 Solution

This chatbot:
- retrieves relevant IVF medical content from PDFs/DOCX/Web sources
- converts them into embeddings
- stores them in a FAISS vector database
- performs semantic similarity search
- injects retrieved context into the LLM
- generates grounded healthcare responses

---

# 🏗️ System Architecture

## High Level Design (HLD)

![HLD Architecture](assets/architecture/hld.png)

---

## Low Level Design (LLD)

![LLD Architecture](assets/architecture/lld.png)

---

# 🖥️ Application UI

![Streamlit UI](assets/screenshots/ui.png)

---

# ⚡ Core Features

✅ RAG-based healthcare chatbot  
✅ IVF medical knowledge retrieval  
✅ FAISS vector database  
✅ Semantic search using embeddings  
✅ Local inference using Ollama + Mistral  
✅ Streamlit conversational UI  
✅ Chat history management  
✅ Multiple document support  
✅ Healthcare hallucination control  
✅ Short & Detailed response modes  
✅ PDF + DOCX + Web ingestion  
✅ Local/private deployment support  

---

# 🧠 Tech Stack

| Component | Technology |
|---|---|
| Frontend | Streamlit |
| Backend | Python |
| Framework | LangChain |
| Vector Database | FAISS |
| Embeddings | all-MiniLM-L6-v2 |
| LLM | Mistral (Ollama) |
| NLP | SentenceTransformers |
| Document Loaders | PyPDF, DOCX Loader |
| Semantic Search | FAISS Similarity Search |

---

# 📂 Project Structure

```bash
ivf-ai-chatbot-rag/
│
├── app.py
├── ingest.py
├── rag_chain.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── data/
│   ├── pdfs/
│   ├── docs/
│
├── assets/
│   ├── architecture/
│   ├── screenshots/
│   └── demo/
│
├── portfolio_site/
│
└── faiss_index/
```

---

# 🔄 RAG Pipeline Flow

## Step 1 — Document Ingestion
Medical PDFs, DOCX files, and trusted healthcare websites are loaded.

## Step 2 — Text Chunking
Documents are split into smaller chunks for efficient retrieval.

## Step 3 — Embedding Generation
Each chunk is converted into vector embeddings using:
```python
all-MiniLM-L6-v2
```

## Step 4 — Vector Storage
Embeddings are stored in a FAISS vector database.

## Step 5 — User Query
The user asks an IVF-related question.

## Step 6 — Semantic Retrieval
Relevant document chunks are retrieved using similarity search.

## Step 7 — Prompt Augmentation
Retrieved context is injected into the LLM prompt.

## Step 8 — Response Generation
Mistral generates a grounded medical response.

---

# 🛡️ Healthcare Safety Features

Since this is a healthcare project, hallucination control was extremely important.

Implemented safeguards:

- Temperature control
- Context-grounded prompting
- No diagnosis instructions
- Source-filtered responses
- Retrieval-only generation
- Trusted medical documents only
- Deterministic response generation

---

# 📚 Knowledge Sources

The chatbot uses:
- IVF medical PDFs
- IVF counseling documents
- Fertility treatment documents
- Trusted healthcare websites
- Research papers
- IVF clinic workflow documents

---

# 📸 Screenshots

## Chat Interface

![Chat UI](assets/screenshots/chatbot.png)

---

## Ingestion Pipeline

![Ingest Pipeline](assets/architecture/ingest.png)

---

# 🎥 Demo

## Project Demo Video
📹 `assets/demo/demo.mp4`

## Technical Explanation Video
📹 `assets/demo/explanation.mp4`

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/ivf-ai-chatbot-rag.git
```

---

## Create Virtual Environment

```bash
python -m venv .venv
```

---

## Activate Environment

### Windows
```bash
.venv\Scripts\activate
```

### Linux / Mac
```bash
source .venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🧱 Build Vector Database

Run ingestion pipeline:

```bash
python ingest.py
```

This:
- loads documents
- creates embeddings
- builds FAISS vector index

---

# ▶️ Run Application

```bash
streamlit run app.py
```

---

# 🧪 Example Questions

- What is IVF?
- How long does an IVF cycle take?
- Can women with PCOS undergo IVF?
- What are IVF success rates?
- Is IVF painful?
- What is ICSI?
- Can IVF help with low sperm count?

---

# 🧠 Interview Explanation Section

# ❓ Why did you use RAG instead of Fine-Tuning?

### Answer:
Fine-tuning is expensive, harder to update, and still prone to hallucinations.

RAG was chosen because:
- knowledge can be updated dynamically
- responses remain grounded in source documents
- no retraining required
- better explainability
- safer for healthcare applications

---

# ❓ Why FAISS?

### Answer:
FAISS provides:
- extremely fast vector similarity search
- efficient local deployment
- low latency retrieval
- no external API dependency
- privacy preservation for medical data

---

# ❓ Why all-MiniLM-L6-v2?

### Answer:
This embedding model:
- lightweight
- CPU efficient
- fast inference
- high semantic similarity accuracy
- ideal for local RAG systems

It generates 384-dimensional embeddings optimized for semantic retrieval.

---

# ❓ Why Ollama + Mistral?

### Answer:
Using local LLM inference:
- reduces API cost
- improves privacy
- enables offline usage
- gives infrastructure control
- supports healthcare compliance scenarios

---

# ❓ How did you reduce hallucinations?

### Answer:
Hallucinations were reduced using:
- retrieval-grounded prompting
- low temperature
- trusted medical sources
- context-only answering
- strict prompt rules
- semantic filtering

---

# ❓ Why chunk documents?

### Answer:
Chunking improves:
- retrieval precision
- embedding quality
- semantic relevance
- token efficiency

Without chunking, retrieval becomes noisy and inaccurate.

---

# ❓ Why use embeddings?

### Answer:
Embeddings convert text into numerical vectors capturing semantic meaning.

This allows:
- semantic similarity search
- meaning-based retrieval
- better context matching than keyword search

---

# 📈 Future Improvements

- Conversational memory
- Multi-turn context
- Hybrid search (BM25 + Vector Search)
- Re-ranking models
- Medical citation generation
- LangSmith tracing
- Authentication
- Docker deployment
- Kubernetes deployment
- HuggingFace deployment
- Feedback loop training
- Multilingual IVF support

---

# 🏆 Key Learnings

- RAG architecture
- Vector databases
- Semantic search
- Healthcare AI systems
- Prompt engineering
- LangChain pipelines
- Local LLM deployment
- Streamlit frontend development
- Hallucination mitigation
- AI system architecture

---

# 👨‍💻 Author

**Lucky Singh**

Aspiring Data Scientist & GenAI Developer  
Focused on:
- Healthcare AI
- RAG Systems
- NLP
- Generative AI
- AI Chatbots

---

# ⭐ If You Like This Project

Give it a ⭐ on GitHub.
