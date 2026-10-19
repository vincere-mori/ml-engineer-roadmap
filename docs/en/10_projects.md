# 🎯 10. Pet Projects and Portfolio

> Russian version: [10_projects.md](../ru/10_projects.md)

> 2–3 **strong** GitHub projects do more for an offer than 10 YouTube tutorials. Quality > quantity.

---

## 🏆 What Makes a Project Strong

- ✅ **Real problem**, not an "MNIST classification" tutorial
- ✅ Full cycle: **data → model → deploy → monitoring**
- ✅ Clean code: typing, tests, lint, CI
- ✅ Documentation: **README with an architecture diagram**
- ✅ Metrics and comparison with baseline
- ✅ Demo: video / Telegram bot / hosted service
- ✅ **Reproducibility** (`docker-compose up`)

---

## 💡 Project Ideas: Junior to Middle

### 🟢 Starter level (1–2 projects during Classical ML)
1. **Apartment price prediction in your city** — CIAN/Avito parsing → CatBoost → SHAP → FastAPI
2. **Resume classifier** — infer candidate grade from vacancy text via hh.ru API
3. **Churn prediction** on an open dataset → MLflow + Airflow for retraining

### 🟡 Middle level (Deep Learning)
4. **CV classification / detection** on your own dataset: plant species, road signs, etc.
5. **NLP review classification** in Russian with RuBERT fine-tuning
6. **Your own nanoGPT** trained on a Russian literature corpus, with process notes in README

### 🔴 "They will consider you for Middle" level
7. **🔥 RAG bot over your own domain knowledge base** — Qdrant + GigaChat/YandexGPT + Telegram
8. **🔥 Recommender** for anime/movies/books — two-tower + ANN (FAISS) + A/B simulation
9. **🔥 End-to-end MLOps platform** — model + DVC + MLflow + k8s + Prometheus + Evidently
10. **🔥 Fine-tune an open LLM (Qwen3 / T-Pro / GigaChat 3) through LoRA** for a concrete task + vLLM serving + your own eval set
11. **🔥 Agent with MCP tools** — e.g. an assistant over your own DB or API, with Langfuse tracing and quality evaluation

### 🤖 Robotics + ML, if the area is interesting
12. **RL agent** for a manipulator in simulation (Isaac Sim / MuJoCo)
13. **Robot CV**: detection + tracking + grasp prediction
14. **VLA (Vision-Language-Action)** — fine-tune an open VLA (OpenVLA, π0 / LeRobot) in simulation

---

## 📁 Project README Template

````markdown
# Project Name

> One-liner about the project

## 🎯 Task and Motivation
…

## 🏗️ Architecture
[architecture diagram — mermaid or image]

## 📊 Results
| Metric | Baseline | My model |
|---|:---:|:---:|
| F1 | 0.72 | **0.83** |
| Latency p99 | 220 ms | **45 ms** |

## 🚀 Run
```bash
docker-compose up
```

## 🧰 Stack
Python, PyTorch, FastAPI, Docker, …

## 📚 What was used
- dataset: …
- model: …
- paper links: …
````

---

## 🏆 Kaggle / Competitions

- 🥉 **Bronze** in tabular data — realistic goal in 2–3 months
- 🥈 Silver — already a strong Middle-level signal
- Russian analogues: **AI Journey Contest** (Sber), **Yandex Cup** (ML track), **DataFest** competitions

---

## 🌟 GitHub Profile

- [ ] Pin 3–6 best repos
- [ ] Filled bio with CV/Telegram link
- [ ] Custom profile README (`username/username` repo)
- [ ] Contributions to open source, even issues/docs, are a **big plus**
  - PyTorch, Hugging Face, vLLM, Qdrant, CatBoost, ClearML

---

<!-- nav -->
← Back: [💼 9. Career in the Russian Market](09_career.md) · [Contents](../../README.md) · Next: [📖 11. Resources, Mostly RU](11_resources.md) →
