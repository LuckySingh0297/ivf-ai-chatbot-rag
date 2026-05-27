# 🧬 IVF AI Chatbot (RAG-Based Healthcare Assistant)

> AI-powered IVF healthcare chatbot using Retrieval-Augmented Generation (RAG), FAISS, LangChain, SentenceTransformers, Ollama, and Streamlit for document-grounded medical question answering.

---

# 🚀 Live Project Overview

The **IVF AI Chatbot** is a healthcare-focused Generative AI application designed to provide accurate, context-aware, and document-grounded responses for IVF-related questions.

The project combines:
- Semantic Search
- Vector Databases
- Retrieval-Augmented Generation (RAG)
- Local LLM Inference
- Healthcare Safety Guardrails

to create a reliable IVF patient support assistant.

Unlike traditional AI chatbots that hallucinate, this system retrieves information directly from verified IVF medical documents before generating responses.

---

# 📌 Problem Statement

Patients undergoing IVF treatment often face:

- Anxiety due to lack of instant medical guidance
- Difficulty understanding medical terminology
- Inconsistent information from online sources
- Long waiting times for consultations
- Limited support outside clinic hours

Traditional LLM-based chatbots may generate:
- inaccurate responses
- hallucinated medical information
- unsafe healthcare advice

This project solves that problem using **Retrieval-Augmented Generation (RAG)**.

---

# 💡 Proposed Solution

The chatbot:
1. Loads IVF medical documents
2. Converts them into embeddings
3. Stores embeddings inside FAISS vector database
4. Performs semantic similarity search
5. Retrieves relevant medical context
6. Injects retrieved context into the LLM prompt
7. Generates grounded healthcare responses

This significantly reduces hallucination and improves factual accuracy.

---

# 🏗️ System Architecture

# 🔹 High Level Design (HLD)

![HLD](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/hld.png)

---

# 🔹 Low Level Design (LLD)

![LLD](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/lld.png)

---

# 🔹 RAG Pipeline Flow

![Pipeline](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/ingest.png)

---

# 🖥️ Application UI

![UI](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/app.png)

---

# 🤖 Chatbot Logic

![Chatbot](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/chatbot.png)

---

# 🎥 Project Demo Videos

# ▶️ Full Project Demo

[🎬 Watch Demo Video](https://github.com/LuckySingh0297/ivf-ai-chatbot-rag/blob/main/Presentation/presentation%20demo%20video.mp4)

---

# ▶️ Additional Videos

[📂 View All Videos](https://github.com/LuckySingh0297/ivf-ai-chatbot-rag/tree/main/Videos)

---

# ⚡ Key Features

✅ RAG-based healthcare chatbot  
✅ IVF medical knowledge retrieval  
✅ FAISS vector database  
✅ Semantic search using embeddings  
✅ Local LLM inference using Ollama + Mistral  
✅ Streamlit conversational UI  
✅ Chat history management  
✅ Multiple document ingestion  
✅ PDF + DOCX + Web support  
✅ Hallucination reduction pipeline  
✅ Healthcare-safe prompting  
✅ Context-grounded answer generation  
✅ Short & Detailed response modes  
✅ Local/private deployment support  

---

# 🧠 Tech Stack

| Component | Technology |
|---|---|
| Frontend | Streamlit |
| Backend | Python |
| Framework | LangChain |
| Vector Database | FAISS |
| Embedding Model | all-MiniLM-L6-v2 |
| LLM | Mistral via Ollama |
| NLP | SentenceTransformers |
| Document Loaders | PyPDFLoader, DOCX Loader |
| Semantic Search | FAISS Similarity Search |
| Prompt Engineering | LangChain Prompt Templates |

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
├── Images/
│   ├── hld.png
│   ├── lld.png
│   ├── app.png
│   ├── chatbot.png
│   └── ingest.png
│
├── Videos/
│
├── Presentation/
│
├── data/
│   ├── pdfs/
│   └── docs/
│
└── faiss_index/
```

---

# 🔄 RAG Workflow

# Step 1 — Document Ingestion

Medical PDFs, DOCX files, and trusted IVF websites are loaded.

Supported Sources:
- IVF PDFs
- Research papers
- DOCX documents
- IVF counseling documents
- Trusted healthcare websites

---

# Step 2 — Text Chunking

Documents are split into smaller semantic chunks.

Why?
- Improves retrieval precision
- Better semantic understanding
- More accurate context matching

---

# Step 3 — Embedding Generation

Each chunk is converted into vector embeddings using:

```python
all-MiniLM-L6-v2
```

The embedding model captures semantic meaning instead of simple keywords.

---

# Step 4 — Vector Storage

Embeddings are stored inside:

```python
FAISS Vector Database
```

FAISS enables:
- extremely fast similarity search
- low latency retrieval
- local deployment
- efficient semantic matching

---

# Step 5 — User Query

The user asks an IVF-related question.

Example:
```text
What is IVF and how does it work?
```

---

# Step 6 — Semantic Similarity Search

The query embedding is matched against document embeddings.

Top relevant chunks are retrieved using cosine similarity.

---

# Step 7 — Prompt Augmentation

Retrieved medical context is injected into the LLM prompt.

This ensures:
- grounded responses
- reduced hallucinations
- document-aware generation

---

# Step 8 — Response Generation

The Mistral LLM generates a healthcare response using retrieved context only.

---

# 🛡️ Healthcare Safety & Hallucination Control

Healthcare AI systems require strong hallucination prevention.

Implemented safeguards:

✅ Context-grounded prompting  
✅ Retrieval-only generation  
✅ Trusted medical sources  
✅ No diagnosis instructions  
✅ Controlled generation rules  
✅ Semantic filtering  
✅ Deterministic prompting strategy  

---

# 📚 Knowledge Base Sources

The chatbot uses:
- IVF medical research papers
- IVF counseling documents
- Fertility treatment guides
- IVF clinic workflow documents
- WHO/NHS healthcare content
- Trusted IVF PDFs and DOCX files

---

# 📸 Screenshots

# 🔹 Main Chat Interface

![Chat Interface](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/app.png)

---

# 🔹 Ingestion Pipeline

![Ingestion](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/ingest.png)

---

# 🔹 Chatbot Retrieval Logic

![Retrieval Logic](https://raw.githubusercontent.com/LuckySingh0297/ivf-ai-chatbot-rag/main/Images/chatbot.png)

---

# ⚙️ Installation

# Clone Repository

```bash
git clone https://github.com/LuckySingh0297/ivf-ai-chatbot-rag.git
```

---

# Create Virtual Environment

```bash
python -m venv .venv
```

---

# Activate Environment

## Windows

```bash
.venv\Scripts\activate
```

## Linux / Mac

```bash
source .venv/bin/activate
```

---

# Install Dependencies

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
- chunks text
- creates embeddings
- stores vectors in FAISS

---

# ▶️ Run Application

```bash
streamlit run app.py
```

---

# 🧪 Example Questions

- What is IVF?
- How long does IVF take?
- Is IVF painful?
- Can PCOS patients undergo IVF?
- What are IVF success rates?
- What is ICSI?
- Can IVF help low sperm count?
- Is IVF safe for women over 40?

---

# 🧠 Interview Explanation Section

# ❓ Why did you use RAG instead of Fine-Tuning?

### Answer

Fine-tuning:
- is expensive
- harder to maintain
- requires retraining
- still hallucinates

RAG was chosen because:
- knowledge updates dynamically
- responses stay grounded in documents
- no retraining required
- explainability improves
- safer for healthcare systems

---

# ❓ Why FAISS?

### Answer

FAISS provides:
- fast vector similarity search
- low latency retrieval
- local deployment
- efficient semantic matching
- privacy preservation for medical data

---

# ❓ Why all-MiniLM-L6-v2?

### Answer

This embedding model:
- lightweight
- CPU efficient
- fast inference
- strong semantic understanding
- ideal for local RAG systems

It generates 384-dimensional embeddings optimized for semantic retrieval.

---

# ❓ Why Ollama + Mistral?

### Answer

Local inference provides:
- reduced API cost
- better privacy
- offline capability
- infrastructure control
- healthcare compliance benefits

---

# ❓ How did you reduce hallucinations?

### Answer

Hallucination reduction techniques:
- retrieval-grounded prompting
- trusted medical documents
- semantic retrieval
- low randomness prompting
- context-only generation
- strict response rules

---

# ❓ Why chunk documents?

### Answer

Chunking improves:
- retrieval accuracy
- semantic matching
- embedding quality
- token efficiency

Without chunking:
- retrieval becomes noisy
- relevant context may be lost

---

# ❓ Why use embeddings?

### Answer

Embeddings convert text into semantic vectors.

This enables:
- meaning-based search
- semantic retrieval
- contextual matching

instead of simple keyword search.

---

# 📈 Future Improvements

- Conversational memory
- Hybrid Search (BM25 + Vector Search)
- Re-ranking models
- LangSmith tracing
- Medical citation generation
- Authentication system
- Docker deployment
- Kubernetes deployment
- HuggingFace deployment
- Feedback learning system
- Multilingual IVF support
- Cloud deployment

---

# 🏆 Key Learnings

- Retrieval-Augmented Generation (RAG)
- Vector databases
- Semantic search
- Healthcare AI systems
- Prompt engineering
- LangChain orchestration
- Local LLM deployment
- Streamlit frontend development
- Hallucination mitigation
- AI system architecture

---

# 🎯 Resume Value of This Project

This project demonstrates:
- Generative AI Engineering
- RAG pipeline development
- NLP understanding
- LLM orchestration
- Healthcare AI applications
- Vector databases
- Semantic search systems
- Production-style AI architecture
- End-to-end AI project deployment

---

# 👨‍💻 Author

# Lucky Singh

Aspiring Data Scientist & GenAI Developer

Focused on:
- Healthcare AI
- Generative AI
- RAG Systems
- NLP
- AI Chatbots
- Vector Databases

---

# ⭐ Support

If you found this project useful:

⭐ Star the repository on GitHub.
```
