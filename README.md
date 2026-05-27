# 🧬 IVF AI Chatbot (RAG-Based Healthcare Assistant)

## 📌 Project Overview

The IVF AI Chatbot is a healthcare-focused Generative AI application built using Retrieval-Augmented Generation (RAG). The system retrieves information from trusted IVF medical documents and generates grounded, context-aware responses for users.

This project combines:
- RAG Architecture
- Semantic Search
- Vector Databases
- Open Source LLMs
- Healthcare AI Safety

to create an intelligent IVF patient support assistant.

---

# 🚀 Key Features

- IVF healthcare chatbot
- Retrieval-Augmented Generation (RAG)
- FAISS vector database
- Semantic similarity search
- Local LLM inference using Ollama
- Streamlit frontend
- PDF and DOCX ingestion
- Context-grounded answer generation
- Reduced hallucination pipeline
- Healthcare-safe prompting

---

# 🏗️ Architecture Flow

User Query → Embedding → Vector Search → Context Retrieval → LLM → Final Response

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

---

# 🔄 RAG Pipeline

1. Document Ingestion
2. Text Chunking
3. Embedding Generation
4. Vector Storage
5. Semantic Retrieval
6. Prompt Augmentation
7. Response Generation

---

# ⚙️ Installation

```bash
git clone https://github.com/LuckySingh0297/ivf-ai-chatbot-rag.git
```

```bash
pip install -r requirements.txt
```

```bash
python ingest.py
```

```bash
streamlit run app.py
```

---

# 🛡️ Hallucination Reduction

- Retrieval-grounded generation
- Trusted medical documents
- Semantic similarity retrieval
- Controlled prompting
- Context-only response generation

---

# 📈 Future Improvements

- Hybrid Search
- Multilingual Support
- Authentication System
- Docker Deployment
- Cloud Deployment
- Citation Generation
- Conversational Memory

---

# 👨‍💻 Author

Lucky Singh

Aspiring Data Scientist & GenAI Developer

Focus Areas:
- Generative AI
- Healthcare AI
- RAG Systems
- NLP
- AI Chatbots
