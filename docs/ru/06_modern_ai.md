# 💬 6. Modern AI — NLP, LLM, RAG

> English version: [06_modern_ai.md](../en/06_modern_ai.md)

> Самая горячая и **самая высокооплачиваемая** ниша 2026. В РФ — Yandex (YandexGPT, Алиса), Sber (GigaChat, Kandinsky), T-Bank, MTS AI, Avito.

---

## 📝 Классический NLP

- [ ] Токенизация (BPE, WordPiece, SentencePiece)
- [ ] Word embeddings: Word2Vec, GloVe, FastText
- [ ] TF-IDF, BM25 (важно для RAG!)
- [ ] Named Entity Recognition, sentiment analysis
- [ ] spaCy, NLTK, Natasha (RU NLP)

---

## 🔥 Transformers

- [ ] **Attention is All You Need** — прочитать **сам** оригинал
- [ ] Self-attention, multi-head, positional encoding (RoPE, ALiBi)
- [ ] Encoder (BERT) vs Decoder (GPT) vs Encoder-Decoder (T5)
- [ ] Pre-training: MLM, CLM, NSP
- [ ] Fine-tuning vs prompt engineering vs in-context learning

---

## 🤖 Large Language Models

- [ ] Архитектура GPT-style моделей
- [ ] Scaling laws (Chinchilla)
- [ ] Tokenization трюки, KV-cache
- [ ] **Instruction tuning, RLHF, DPO**
- [ ] Quantization (GPTQ, AWQ, bitsandbytes)
- [ ] **PEFT / LoRA / QLoRA** — fine-tune на своём железе
- [ ] **Reasoning-модели и RL-дообучение**: chain-of-thought, test-time compute, GRPO / RLVR
- [ ] Архитектурные тренды: MoE, GQA/MLA, длинный контекст, FlashAttention
- [ ] Inference оптимизация: **vLLM**, **SGLang**, llama.cpp, speculative decoding, **Triton Inference Server** (TGI с 2026 в архиве)
- [ ] Structured outputs (JSON schema), constrained decoding
- [ ] **Evals**: бенчмарки, LLM-as-a-judge, свой eval-набор под задачу; русские бенчмарки MERA, ruMTEB

### Российские LLM
- [ ] **YandexGPT** API, **GigaChat** API (Sber)
- [ ] Открытые веса: **GigaChat 3** (`ai-sage`, MoE), **T-Pro 2.0** (`t-tech`), **YandexGPT-5-Lite-8B** (`yandex`)
- [ ] На практике в РФ часто дообучают открытые **Qwen3** и подобные; Saiga (Илья Гусев) как пример русификации

---

## 🔎 RAG (Retrieval-Augmented Generation)

> Самый востребованный паттерн в продуктах 2025–2026. Всё чаще в связке с агентами (agentic RAG).

- [ ] Pipeline: chunking → embeddings → vector DB → retrieve → rerank → generate
- [ ] Embedding модели (e5, BGE-M3), русские: `ai-forever/FRIDA`, `ai-sage/Giga-Embeddings-instruct`, `deepvk/USER-bge-m3`, `intfloat/multilingual-e5` (сравнивать по ruMTEB)
- [ ] **Vector DB**: **Qdrant**, Milvus, pgvector
- [ ] Hybrid search (BM25 + dense)
- [ ] Rerankers (Cohere, BGE-reranker)
- [ ] Frameworks: **LangChain**, **LlamaIndex**, **Haystack**
- [ ] Оценка качества RAG (ragas, своя golden dataset)

---

## 👁️ Современный CV

- [ ] CLIP / SigLIP, SAM 2, DINOv3
- [ ] VLM: Qwen-VL, LLaVA (как учебная архитектура)
- [ ] Diffusion и flow matching: SD, FLUX, ControlNet, LoRA
- [ ] **Kandinsky** (Sber) — open-source, можно дообучать

---

## 🤝 Agents

- [ ] Function/tool calling
- [ ] ReAct, plan-and-execute
- [ ] Фреймворки: LangGraph, PydanticAI, smolagents (CrewAI / AutoGen обзорно)
- [ ] **MCP (Model Context Protocol)** — стандарт подключения инструментов
- [ ] Оценка и трейсинг агентов: Langfuse, Arize Phoenix
- [ ] Безопасность: prompt injection, guardrails

---

## 📚 Ресурсы

| Ресурс | Уровень |
|---|:---:|
| 🥇 [Hugging Face LLM Course](https://huggingface.co/learn/llm-course) | ⭐⭐ |
| 🥇 [Stanford CS336 — Language Modeling from Scratch](https://stanford-cs336.github.io/) | ⭐⭐⭐ |
| 🥇 [Stanford CS224n](https://web.stanford.edu/class/cs224n/) | ⭐⭐⭐ |
| 🎥 Andrej Karpathy — «Let's build GPT» / nanoGPT / [nanochat](https://github.com/karpathy/nanochat) | ⭐⭐⭐ |
| 📘 «Build a Large Language Model from Scratch» — Sebastian Raschka ([код бесплатно](https://github.com/rasbt/LLMs-from-scratch)) | ⭐⭐⭐ |
| 📘 «AI Engineering» — Chip Huyen, 2025 | ⭐⭐ |
| 📚 [The Ultra-Scale Playbook (HF)](https://huggingface.co/spaces/nanotron/ultrascale-playbook) — распределённое обучение LLM | ⭐⭐⭐ |
| 🎥 [karpov.courses — NLP / LLM](https://karpov.courses/) | ⭐⭐ |
| 📚 [ai-russia.ru](https://ai-russia.ru/) — Альянс в сфере ИИ, витрина ИИ-кейсов российских компаний | ⭐ |

---

## ✅ Контрольные проекты

1. С нуля написать **GPT-mini** (по nanoGPT) и обучить на русском датасете.
2. **RAG-бот по своей базе знаний**: документы → Qdrant → YandexGPT/GigaChat → Telegram-бот.
3. **Fine-tune открытой модели (Qwen3 / T-Pro / GigaChat 3)** через LoRA на своей задаче, задеплоить через vLLM и сравнить с базой на своём eval-наборе.

---

<!-- nav -->
← Назад: [🧠 5. Deep Learning](05_deep_learning.md) · [Оглавление](../../README.md) · Далее: [⚙️ 7. MLOps & Production](07_mlops.md) →
