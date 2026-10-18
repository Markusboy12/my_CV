# Mark A. Rakhmanov · [English](README_EN.md)

**Data Scientist / ML Engineer — NLP, LLMs & Generative AI**

Moscow / Moscow Region · Open to remote, hybrid, or on-site opportunities

[![Email](https://img.shields.io/badge/Email-markrahmanov958%40gmail.com-blue?style=flat-square&logo=gmail)](mailto:markrahmanov958@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Markusboy12-black?style=flat-square&logo=github)](https://github.com/Markusboy12)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-LadiesMan69-yellow?style=flat-square)](https://huggingface.co/LadiesMan69)

---

## 🧑‍💻 Professional Profile

Data Scientist / ML Engineer focused on NLP, Large Language Models (LLMs), and Generative AI. Build end-to-end ML/LLM pipelines spanning fine-tuning and parameter-efficient fine-tuning (LoRA/QLoRA), RAG, embeddings, vector search, LLM inference, and deployment. Fine-tuned and adapted DeepSeek, Qwen, and Phi-3; publish models on Hugging Face, including low-resource NLP work. Built a RAG system with measured citation accuracy (85%, n=50) and am developing a coding agent with long-term memory and self-debugging.

---

## 🛠 Core Skills

| Category | Skills |
|---|---|
| **LLM / NLP** | Hugging Face Transformers, fine-tuning, LoRA, QLoRA, PEFT, DeepSeek, Qwen, Phi-3, prompt engineering, SentenceTransformers, low-resource NLP |
| **RAG / Information Retrieval** | RAG, embeddings, vector search (Qdrant), document parsing, chunking, retrieval, citation evaluation |
| **ML / DL** | Python (OOP), PyTorch, Scikit-learn, Pandas, NumPy, feature engineering, model evaluation |
| **LLM Inference / MLOps** | vLLM, Ollama, quantization, FastAPI, Docker, MLflow, Git, Inngest, Streamlit, remote GPU servers (SSH) |
| **Agentic AI** | LLM agents, RAG-based memory, tool use / function calling, LLM provider orchestration (OpenRouter), self-debugging; learning MCP |
| **Data / Backend** | SQL, PostgreSQL, REST APIs |

---

## 🚀 Featured Projects

### 📄 PDF Document Analysis RAG System

`Python` · `FastAPI` · `Qdrant` · `SentenceTransformers` · `Llama-3-70B` · `Inngest` · `Streamlit`

🔗 [github.com/Markusboy12/RAG_69](https://github.com/Markusboy12/RAG_69)

- Built an end-to-end RAG pipeline: PDF parsing → chunking → embeddings (`all-MiniLM-L6-v2`) → Qdrant indexing → retrieval → answer generation with Llama-3-70B.
- Implemented a FastAPI backend, asynchronous ingestion and generation with Inngest, and a Streamlit UI displaying answer sources.
- **Result:** Manual evaluation on a sample of 50 queries showed **85% citation accuracy** and answer generation in **under 3 seconds**.

---

### ⚙️ FastAPI RAG Agent with Hybrid Search

`Python 3.11` · `FastAPI` · `LangGraph` · `Qdrant` · `BM25` · `RRF` · `Jina Reranker` · `Streamlit` · `Docker`

🔗 [github.com/Markusboy12/RAG_fastapi](https://github.com/Markusboy12/RAG_fastapi)

- Built a RAG system with a FastAPI backend and Streamlit UI, combining LLM-based query rewriting, hybrid retrieval (Qdrant vector search + BM25), Reciprocal Rank Fusion (RRF), and reranking.
- Implemented fault-tolerant fallback chains for LLMs, embeddings, reranking, and answer generation, including offline operation when external providers are unavailable.
- Added response caching (in-memory or Redis/Upstash), CLI-based document indexing, OpenAPI/Swagger documentation, and Docker Compose for running the services.
- Implemented evaluation metrics including Recall@K, MRR, nDCG@K, faithfulness, and answer relevancy; tests cover retrieval, fusion, the query pipeline, and document extraction.
- **Demo-corpus results:** Recall@5, MRR, and nDCG@5 were 1.0. These results come from a small corpus of 3 chunks and 8 queries and should not be interpreted as real-world performance.

---

### 🌍 LLM Adaptation for Tatar (Low-Resource NLP)

`DeepSeek` · `Qwen2.5` · `Hugging Face`

🔗 [huggingface.co/LadiesMan69](https://huggingface.co/LadiesMan69)

- Adapted open-source LLMs (DeepSeek, Qwen2.5) for the Tatar language and published models and related tools on Hugging Face.
- **Result:** **200+ downloads**, with hands-on experience in multilingual models and language/domain adaptation.

---

### 🎮 Hackathon: LLM Characters for a High-Speed Rail Gamification Simulator

`LLM fine-tuning` · `vLLM` · `Remote GPU server (SSH)` · `OpenRouter`

- Worked on an interactive train simulator where players move between carriages and have live conversations with characters. Fine-tuned an LLM to play multiple NPCs from a predefined character list; model metrics were promising, with further system-prompt tuning remaining.
- Rented a GPU server, connected remotely over SSH, and deployed the fine-tuned model using vLLM; requests through a shared API key returned appropriate responses.
- **Result:** The end-to-end pipeline worked. When the inference service stalled near the deadline, the team switched to a hosted LLM through OpenRouter to keep the demo running.

---

### 🩺 Medical LLM Fine-Tuning

`Phi-3-mini` · `PyTorch` · `Unsloth` · `Hugging Face` · `LoRA`

🔗 [github.com/Markusboy12/Phi-3-fine-tuned](https://github.com/Markusboy12/Phi-3-fine-tuned)

- Fine-tuned Phi-3-mini on a medical dataset using LoRA and built a reproducible, modular training pipeline.
- **Result:** Unsloth approximately **doubled training speed** and reduced memory usage; training was run on a free Google Colab T4 GPU.

---

### 🤖 Coding Agent with Memory and Self-Debugging (In Progress)

`Python` · `RAG` · `LLMs` · `Multi-provider orchestration`

- Developing a coding agent with a self-debugging loop and long-term RAG-based memory; designing interactions between LLMs, tools, and external context.
- Experimenting with tool use / function calling, orchestration across multiple LLM providers, and practical model comparisons.

---

### 💳 Credit Scoring Service

`Python` · `Scikit-learn` · `Pandas` · `FastAPI` · `Streamlit`

🔗 [github.com/Markusboy12/Scoring_service](https://github.com/Markusboy12/Scoring_service)

- Built an end-to-end ML pipeline covering EDA, feature engineering, and logistic regression, deployed through FastAPI and Streamlit.
- **Result:** **Recall 67%**.

---

## 🎓 Education & Languages

**Russian University of Cooperation** — Information Systems and Programming  
*Expected graduation: 2028*

Relevant coursework: probability and mathematical statistics, advanced and discrete mathematics, algorithms and programming.

**Languages**
- Russian — Native
- English — B2 (technical documentation, datasets, and models)

---

## 📬 Contact

- **Email:** [markrahmanov958@gmail.com](mailto:markrahmanov958@gmail.com)
- **GitHub:** [github.com/Markusboy12](https://github.com/Markusboy12)
- **Hugging Face:** [huggingface.co/LadiesMan69](https://huggingface.co/LadiesMan69)

---

*Resume updated: October 2026*
