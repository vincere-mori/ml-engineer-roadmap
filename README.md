<div align="center">

# 🤖 ML Engineer Roadmap 2026

### Roadmap to Senior ML Engineer in the Russian market

[Русская версия](docs/ru/01_foundations.md) · [English version](docs/en/01_foundations.md)

![Status](https://img.shields.io/badge/status-active-success?style=for-the-badge)
![Level](https://img.shields.io/badge/level-junior%E2%86%92senior-blue?style=for-the-badge)
![Market](https://img.shields.io/badge/market-Russia%20%F0%9F%87%B7%F0%9F%87%BA-red?style=for-the-badge)
![Updated](https://img.shields.io/badge/updated-2026--10-orange?style=for-the-badge)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![CatBoost](https://img.shields.io/badge/CatBoost-FFCC00?style=flat-square&logo=catboost&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/K8s-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)

</div>

---

## 📍 About the roadmap

A practical path from zero to an ML Engineer offer, tuned for the Russian job market: which stack companies here actually use, where to apply, what they ask in interviews, and what to read.

Each section is a checklist. Tick things off as you go, and at the bottom of every page there are links to the previous and next sections, so you can read it like a book.

The docs come in two languages, [Русский](docs/ru/01_foundations.md) and [English](docs/en/01_foundations.md). The content is the same.

---

## 🗺️ Roadmap

```mermaid
flowchart TD
    A[🚀 Start] --> B[1️⃣ Foundations<br/>Python · Math · CS]
    B --> C[2️⃣ Data<br/>SQL · Pandas · Spark]
    C --> D[3️⃣ Classical ML<br/>sklearn · CatBoost · XGBoost]
    D --> E[4️⃣ Deep Learning<br/>PyTorch · CV · NLP]
    E --> F[5️⃣ Modern AI<br/>Transformers · LLM · RAG]
    D --> G[6️⃣ MLOps<br/>Docker · K8s · MLflow · CI/CD]
    F --> G
    G --> H[7️⃣ System Design<br/>for ML systems]
    H --> I[💼 Junior ML Engineer<br/>120–200k ₽]
    I --> J[💼 Middle ML Engineer<br/>200–350k ₽]
    J --> K[💼 Senior / Lead<br/>350–800k+ ₽]

    style A fill:#4A90E2,stroke:#fff,color:#fff
    style I fill:#27AE60,stroke:#fff,color:#fff
    style J fill:#16A085,stroke:#fff,color:#fff
    style K fill:#8E44AD,stroke:#fff,color:#fff
```

---

## 📚 Stages

| # | Section | Duration | EN | RU |
|---|---|:---:|---|---|
| 1 | 🐍 **Foundations** — Python, algorithms, CS | 1–2 months | [en](docs/en/01_foundations.md) | [ru](docs/ru/01_foundations.md) |
| 2 | 📐 **Math for ML** | in parallel | [en](docs/en/02_math.md) | [ru](docs/ru/02_math.md) |
| 3 | 🗄️ **Data Engineering for ML** | 1–2 months | [en](docs/en/03_data.md) | [ru](docs/ru/03_data.md) |
| 4 | 🤖 **Classical ML** | 2–3 months | [en](docs/en/04_classical_ml.md) | [ru](docs/ru/04_classical_ml.md) |
| 5 | 🧠 **Deep Learning** | 2–3 months | [en](docs/en/05_deep_learning.md) | [ru](docs/ru/05_deep_learning.md) |
| 6 | 💬 **NLP, CV, LLM** | 2–3 months | [en](docs/en/06_modern_ai.md) | [ru](docs/ru/06_modern_ai.md) |
| 7 | ⚙️ **MLOps & Production** | 2 months | [en](docs/en/07_mlops.md) | [ru](docs/ru/07_mlops.md) |
| 8 | 🏗️ **ML System Design** | 1 month | [en](docs/en/08_system_design.md) | [ru](docs/ru/08_system_design.md) |
| 9 | 💼 **Career in the Russian market** | continuous | [en](docs/en/09_career.md) | [ru](docs/ru/09_career.md) |
| 10 | 🎯 **Pet projects and portfolio** | continuous | [en](docs/en/10_projects.md) | [ru](docs/ru/10_projects.md) |
| 11 | 📖 **Resources** | — | [en](docs/en/11_resources.md) | [ru](docs/ru/11_resources.md) |

---

## 🎯 Approximate plan

```mermaid
gantt
    title Approximate 12-month plan (axis = month number)
    dateFormat  YYYY-MM-DD
    axisFormat  %m

    section Foundations
    Python advanced + algorithms   :a1, 2026-01-01, 45d
    Math review + statistics       :a2, 2026-01-01, 60d

    section Data
    Advanced SQL + Pandas          :b1, after a1, 30d
    Spark / Airflow basics         :b2, after b1, 30d

    section ML
    Classical ML + Kaggle competition :c1, after b1, 75d
    Deep Learning with PyTorch        :c2, after c1, 75d
    NLP / LLM / RAG                   :c3, after c2, 60d

    section MLOps
    Docker, FastAPI, MLflow, CI/CD :d1, after c2, 45d
    K8s + serving, Triton/vLLM/SGLang :d2, after d1, 30d

    section Career
    Pet projects + GitHub          :e1, 2026-02-01, 300d
    Internship / offer             :e2, 2026-07-01, 180d
```

---

## 💰 Salary benchmarks, Russia 2026

| Grade | Experience | Moscow, gross / month | Regions |
|---|:---:|:---:|:---:|
| 👶 Intern / Trainee | 0 | 60–120k ₽ | 40–80k ₽ |
| 🚀 Junior | 0–1 year | 120–200k ₽ | 90–150k ₽ |
| ⚡ Middle | 2–3 years | 200–350k ₽ | 150–280k ₽ |
| 🔥 Senior | 4–6 years | 350–600k ₽ | 250–450k ₽ |
| 👑 Lead / Staff | 6+ years | 600k–1M+ ₽ | 400–700k ₽ |

> Rough ranges as of 2026. Real numbers swing a lot by company, grade and stack, and LLM/CV roles usually pay above average. Check fresh data before negotiating: [Habr Career salaries](https://career.habr.com/salaries), [getmatch](https://getmatch.ru), [hh.ru](https://hh.ru).

---

## 🏢 Who hires ML Engineers in Russia

<div align="center">

| 🥇 Tier-1 | 🥈 Tier-2 | 🥉 Tier-3 |
|:---:|:---:|:---:|
| Yandex (Search, Alice, Shedevrum) | Avito | Wildberries |
| Sber / SberAI (GigaChat, Kandinsky) | Ozon | X5 Tech |
| T-Bank | MTS AI / MWS | Alfa-Bank |
| VK (VK Tech, Marusia) | Kaspersky | Gazprombank Tech |
| | Skoltech / AIRI | VTB, Sovcombank |

</div>

---

## ✅ Interview readiness checklist

- [ ] Python: OOP, async, typing, tests (`pytest`)
- [ ] Algorithms: ~150 LeetCode Easy/Medium problems
- [ ] SQL: window functions, optimization, EXPLAIN
- [ ] Math: linear algebra, calculus, probability, statistics
- [ ] Classical ML: explain bias/variance, regularization, boosting internals
- [ ] Deep Learning: implemented backprop, CNN, Transformer by hand
- [ ] PyTorch: can write a train loop without copy-paste
- [ ] LLM: attention, KV-cache, RAG, fine-tuning (LoRA), evals, agents/MCP
- [ ] MLOps: deployed a model with Docker + FastAPI + monitoring
- [ ] System Design: studied 3+ cases: recommendations, search, fraud, NLP service
- [ ] Portfolio: 2–3 strong pet projects on GitHub
- [ ] Kaggle: 1+ competition with a Bronze+ medal
- [ ] Resume on hh + getmatch + Habr Career

---

## 🧭 How to use this repository

1. Go through sections **in order**, but study math and algorithms **in parallel**.
2. Back every topic with a **project**, ideas are in [10_projects.md](docs/en/10_projects.md).
3. Track your progress: fork the repo and fill in [PROGRESS.md](PROGRESS.md), or open an issue from the "My progress" template in your fork.
4. Most resources are Russian-language and practical for the Russian market.

---

## 🤝 Contributing

Found a dead link, an outdated tool, or know a great resource that's missing? Open an [issue](../../issues/new/choose) or send a PR, see [CONTRIBUTING.md](CONTRIBUTING.md). Links are checked automatically once a month.

---

## 📄 License

The text is licensed under [CC BY-SA 4.0](LICENSE). You can copy, translate and remix it, just credit this repo and keep the same license.

---

<div align="center">

### ⭐ If this roadmap is useful, give it a star

**Made for learning and portfolio building · 2026**

</div>
