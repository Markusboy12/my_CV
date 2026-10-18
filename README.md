# Марк А. Рахманов · [English](README_EN.md)

**Data Scientist / ML Engineer — NLP, LLM, Generative AI**

Москва / Подмосковье · удалённо, гибрид или офис

[![Email](https://img.shields.io/badge/Email-markrahmanov958@gmail.com-blue?style=flat-square&logo=gmail)](mailto:markrahmanov958@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Markusboy12-black?style=flat-square&logo=github)](https://github.com/Markusboy12)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-LadiesMan69-yellow?style=flat-square)](https://huggingface.co/LadiesMan69)

---

## 🧑‍💻 Профессиональный профиль

Data Scientist / ML Engineer с фокусом на NLP, Large Language Models (LLM) и Generative AI. Разрабатываю end-to-end ML/LLM-пайплайны: fine-tuning и parameter-efficient fine-tuning (LoRA/QLoRA), RAG, embeddings, vector search, LLM inference и deployment. Дообучал и адаптировал DeepSeek, Qwen и Phi-3, публикую модели на Hugging Face (включая low-resource NLP), создал RAG-систему с измеренным качеством (citation accuracy 85%, n=50) и разрабатываю LLM-агента с памятью и self-debugging.

---

## 🛠 Ключевые навыки

| Категория | Навыки |
|-----------|--------|
| **LLM / NLP** | Hugging Face Transformers, fine-tuning, LoRA, QLoRA, PEFT, DeepSeek, Qwen, Phi-3, prompt engineering, SentenceTransformers, low-resource NLP |
| **RAG / Information Retrieval** | RAG, embeddings, vector search (Qdrant), document parsing, chunking, retrieval, citation evaluation |
| **ML / DL** | Python (OOP), PyTorch, Scikit-learn, Pandas, NumPy, feature engineering, model evaluation |
| **LLM Inference / MLOps** | vLLM, Ollama, quantization, FastAPI, Docker, MLflow, Git, Inngest, Streamlit, удалённые GPU-серверы (SSH) |
| **Agentic AI** | LLM agents, RAG-память, tool use / function calling, оркестрация LLM-провайдеров (OpenRouter), self-debugging; MCP — в изучении |
| **Data / Backend** | SQL, PostgreSQL, REST API |

---

## 🚀 Ключевые проекты

### 📄 RAG-система для анализа PDF-документов
`Python` · `FastAPI` · `Qdrant` · `SentenceTransformers` · `Llama-3-70B` · `Inngest` · `Streamlit`
🔗 [github.com/Markusboy12/RAG_69](https://github.com/Markusboy12/RAG_69)

- Разработал end-to-end RAG pipeline: PDF parsing → chunking → embeddings (all-MiniLM-L6-v2) → индексация в Qdrant → retrieval → генерация ответа (Llama-3-70B).
- Backend на FastAPI; асинхронная обработка ingestion и генерации через Inngest; интерфейс на Streamlit с отображением источников ответа.
- **Результат:** ручная evaluation на выборке n=50 — точность цитирования источников **85%**, время генерации ответа **менее 3 секунд**.

---

### ⚙️ RAG-агент на FastAPI с гибридным поиском

`Python 3.11` · `FastAPI` · `LangGraph` · `Qdrant` · `BM25` · `RRF` · `Jina Reranker` · `Streamlit` · `Docker`

🔗 [github.com/Markusboy12/RAG_fastapi](https://github.com/Markusboy12/RAG_fastapi)

- Разработал RAG-систему с FastAPI backend и Streamlit UI: переписывание запросов через LLM, гибридный retrieval (векторный поиск Qdrant + BM25), объединение результатов Reciprocal Rank Fusion (RRF) и reranking.
- Реализовал отказоустойчивые fallback-цепочки для LLM, embeddings, reranker и генерации ответа; при недоступности внешних провайдеров система сохраняет возможность отвечать офлайн.
- Добавил кэширование ответов (in-memory или Redis/Upstash), CLI-индексацию документов, API-документацию OpenAPI/Swagger и Docker Compose для запуска сервисов.
- Реализовал оценку качества через Recall@K, MRR, nDCG@K, faithfulness и answer relevancy; тесты проекта покрывают retrieval, fusion, pipeline и извлечение документов.
- **Результат на демонстрационном корпусе:** Recall@5, MRR и nDCG@5 — 1.0; значения получены на небольшом корпусе из 3 чанков и 8 запросов и не являются оценкой качества на реальных данных.

---

### 🌍 Адаптация LLM для татарского языка (Low-Resource NLP)
`DeepSeek` · `Qwen2.5` · `Hugging Face`
🔗 [huggingface.co/LadiesMan69](https://huggingface.co/LadiesMan69)

- Адаптировал современные open-source LLM (DeepSeek, Qwen2.5) под татарский язык; опубликовал модели и связанные инструменты на Hugging Face.
- **Результат:** **200+ загрузок**; практический опыт работы с мультиязычными моделями и адаптацией LLM под язык и домен.

---

### 🎮 Хакатон (Москва): LLM-персонажи для симулятора геймификации ВСМ
`LLM fine-tuning` · `vLLM` · `арендованный GPU-сервер (SSH)` · `OpenRouter`

- **Задача:** интерактивный симулятор поезда, где игрок ходит по вагонам и ведёт живые диалоги с персонажами. Дообучил LLM играть несколько NPC-персонажей из заданного списка; модель показала хорошие метрики, оставалось улучшить системный промпт.
- Арендовал GPU-сервер на время хакатона, работал на нём удалённо по SSH и развернул дообученную модель через vLLM; запросы по одному общему API-ключу возвращали корректные ответы.
- **Результат:** пайплайн работал end to end; когда инференс-сервис завис перед дедлайном, команда перешла на hosted-LLM через OpenRouter, чтобы сохранить демо.

---

### 🩺 Дообучение медицинской LLM
`Phi-3-mini` · `PyTorch` · `Unsloth` · `Hugging Face` · `LoRA`
🔗 [github.com/Markusboy12/Phi-3-fine-tuned](https://github.com/Markusboy12/Phi-3-fine-tuned)

- Дообучил Phi-3-mini на медицинском датасете с помощью LoRA (parameter-efficient fine-tuning); построил воспроизводимый модульный pipeline обучения.
- **Результат:** Unsloth ускорил обучение примерно **в 2 раза** и снизил потребление памяти; обучение выполнено на бесплатном Google Colab T4.

---

### 🤖 Coding Agent с памятью и self-debugging (в разработке)
`Python` · `RAG` · `LLM` · `multi-provider orchestration`

- Разрабатываю coding agent с циклом self-debugging и долгосрочной памятью на базе RAG; проектирую взаимодействие LLM с инструментами и внешним контекстом.
- Экспериментирую с tool use / function calling, оркестрацией нескольких LLM-провайдеров и сравнением моделей по прикладным характеристикам.

---

### 💳 Сервис кредитного скоринга
`Python` · `Scikit-learn` · `Pandas` · `FastAPI` · `Streamlit`
🔗 [github.com/Markusboy12/Scoring_service](https://github.com/Markusboy12/Scoring_service)

- Разработал end-to-end ML pipeline: EDA, feature engineering, логистическая регрессия; deployment через FastAPI + Streamlit.
- **Результат:** **Recall 67%**.

---

## 🎓 Образование и языки

**Российский университет кооперации** — Информационные системы и программирование
*Ожидаемое окончание: 2028*

Дисциплины: теория вероятностей и мат. статистика, высшая и дискретная математика, алгоритмизация и программирование.

**Языки:**
- Русский — родной
- Английский — B2 (техническая документация, датасеты и модели)

---

## 📬 Контакты

- **Email:** [markrahmanov958@gmail.com](mailto:markrahmanov958@gmail.com)
- **Телефон:** [+7 (916) 685-24-34](tel:+79166852434)
- **GitHub:** [github.com/Markusboy12](https://github.com/Markusboy12)
- **Hugging Face:** [huggingface.co/LadiesMan69](https://huggingface.co/LadiesMan69)

---

*Резюме обновлено: октябрь 2026*
