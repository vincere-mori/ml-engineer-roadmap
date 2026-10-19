# 💬 6. Modern AI — NLP, LLM, RAG

> [📋 Contents](../../README.en.md) · [🇷🇺 Русский](../ru/06_modern_ai.md)

> The hottest and **highest-paid** niche in 2026. In Russia: Yandex (YandexGPT, Alice), Sber (GigaChat, Kandinsky), T-Bank, MTS AI, Avito.

---

## 📝 Classical NLP

- [ ] Tokenization (BPE, WordPiece, SentencePiece)
- [ ] Word embeddings: Word2Vec, GloVe, FastText
- [ ] TF-IDF, BM25 (important for RAG!)
- [ ] Named Entity Recognition, sentiment analysis
- [ ] spaCy, NLTK, Natasha (RU NLP)

---

## 🔥 Transformers

- [ ] **Attention is All You Need** — read the original paper **yourself**
- [ ] Self-attention, multi-head, positional encoding (RoPE, ALiBi)
- [ ] Encoder (BERT) vs Decoder (GPT) vs Encoder-Decoder (T5)
- [ ] Pre-training: MLM, CLM, NSP
- [ ] Fine-tuning vs prompt engineering vs in-context learning

---

## 🤖 Large Language Models

- [ ] Architecture of GPT-style models
- [ ] Scaling laws (Chinchilla)
- [ ] Tokenization tricks, KV-cache
- [ ] **Instruction tuning, RLHF, DPO**
- [ ] Quantization (GPTQ, AWQ, bitsandbytes)
- [ ] **PEFT / LoRA / QLoRA** — fine-tune on your own hardware
- [ ] **Reasoning models and RL post-training**: chain-of-thought, test-time compute, GRPO / RLVR
- [ ] Architecture trends: MoE, GQA/MLA, long context, FlashAttention
- [ ] Inference optimization: **vLLM**, **SGLang**, llama.cpp, speculative decoding, **Triton Inference Server** (TGI archived in 2026)
- [ ] Structured outputs (JSON schema), constrained decoding
- [ ] **Evals**: benchmarks, LLM-as-a-judge, your own task eval set; Russian benchmarks MERA, ruMTEB

### Russian LLMs
- [ ] **YandexGPT** API, **GigaChat** API (Sber)
- [ ] Open weights: **GigaChat 3** (`ai-sage`, MoE), **T-Pro 2.0** (`t-tech`), **YandexGPT-5-Lite-8B** (`yandex`)
- [ ] In practice, Russian teams often fine-tune open **Qwen3**-class models; Saiga (Ilya Gusev) as a Russification example

---

## 🔎 RAG (Retrieval-Augmented Generation)

> The most in-demand product pattern in 2025–2026, increasingly combined with agents (agentic RAG).

- [ ] Pipeline: chunking → embeddings → vector DB → retrieve → rerank → generate
- [ ] Embedding models (e5, BGE-M3), Russian: `ai-forever/FRIDA`, `ai-sage/Giga-Embeddings-instruct`, `deepvk/USER-bge-m3`, `intfloat/multilingual-e5` (compare on ruMTEB)
- [ ] **Vector DB**: **Qdrant**, Milvus, pgvector
- [ ] Hybrid search (BM25 + dense)
- [ ] Rerankers (Cohere, BGE-reranker)
- [ ] Frameworks: **LangChain**, **LlamaIndex**, **Haystack**
- [ ] RAG quality evaluation (ragas, your own golden dataset)

---

## 👁️ Modern CV

- [ ] CLIP / SigLIP, SAM 2, DINOv3
- [ ] VLMs: Qwen-VL, LLaVA (as a learning architecture)
- [ ] Diffusion and flow matching: SD, FLUX, ControlNet, LoRA
- [ ] **Kandinsky** (Sber) — open-source, can be fine-tuned

---

## 🤝 Agents

- [ ] Function/tool calling
- [ ] ReAct, plan-and-execute
- [ ] Frameworks: LangGraph, PydanticAI, smolagents (CrewAI / AutoGen as an overview)
- [ ] **MCP (Model Context Protocol)** — the standard way to plug in tools
- [ ] Agent evals and tracing: Langfuse, Arize Phoenix
- [ ] Security: prompt injection, guardrails

---

## 📚 Resources

| Resource | Level |
|---|:---:|
| 🥇 [Hugging Face LLM Course](https://huggingface.co/learn/llm-course) | ⭐⭐ |
| 🥇 [Stanford CS336 — Language Modeling from Scratch](https://stanford-cs336.github.io/) | ⭐⭐⭐ |
| 🥇 [Stanford CS224n](https://web.stanford.edu/class/cs224n/) | ⭐⭐⭐ |
| 🎥 Andrej Karpathy — "Let's build GPT" / nanoGPT | ⭐⭐⭐ |
| 📘 "Build a Large Language Model from Scratch" — Sebastian Raschka ([free code](https://github.com/rasbt/LLMs-from-scratch)) | ⭐⭐⭐ |
| 📘 "AI Engineering" — Chip Huyen, 2025 | ⭐⭐ |
| 📚 [The Ultra-Scale Playbook (HF)](https://huggingface.co/spaces/nanotron/ultrascale-playbook) — distributed LLM training | ⭐⭐⭐ |
| 🎥 [karpov.courses — NLP / LLM](https://karpov.courses/) | ⭐⭐ |
| 📚 [ai-russia.ru](https://ai-russia.ru/) — AI Alliance Russia, showcase of AI cases from Russian companies | ⭐ |

---

## ✅ Checkpoint projects

1. Write **GPT-mini** from scratch (nanoGPT-style) and train it on a Russian dataset.
2. **RAG bot over your own knowledge base**: documents → Qdrant → YandexGPT/GigaChat → Telegram bot.
3. **Fine-tune an open model (Qwen3 / T-Pro / GigaChat 3)** through LoRA for your own task, deploy through vLLM, and compare with the base model on your own eval set.

---

<!-- nav -->
← Back: [🧠 5. Deep Learning](05_deep_learning.md) · [Contents](../../README.en.md) · Next: [⚙️ 7. MLOps & Production](07_mlops.md) →
