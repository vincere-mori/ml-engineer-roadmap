# 🏗️ 8. ML System Design

> Russian version: [08_system_design.md](../ru/08_system_design.md)

> The **interview section** that most often separates Junior from Middle, and Middle from Senior. At Yandex/T-Bank/Avito it is mandatory.

---

## 🧩 Answer Framework

1. **Clarify the task**: business/ML metrics, load, SLA, constraints
2. **Metrics**: business → product → ML offline → ML online
3. **Data**: sources, volume, annotation, labeling, GDPR/152-FZ
4. **Baseline → iterations**: from simple to complex
5. **Features**: feature engineering, feature store
6. **Model**: candidates, choice, validation
7. **Inference**: latency, batching, caching, GPU/CPU
8. **Deployment**: A/B, canary, shadow
9. **Monitoring**: metrics, drift, alerts, retraining
10. **Trade-offs**: what you saved, what you sacrificed

---

## 🎯 Typical Cases to Study

| Case | Where it is asked |
|---|---|
| 📺 **Video/product recommendations** | Yandex Kinopoisk, VK Clips, Wildberries, Ozon |
| 🔎 **Search / ranking** | Yandex Search, Avito, Wildberries |
| 💳 **Anti-fraud / scoring** | T-Bank, Sber, Alfa |
| 📨 **Spam / moderation** | VK, Avito, Yandex Mail |
| 💬 **Chatbot / RAG** | Sber GigaChat, Yandex, T-Bank |
| 🚗 **ETA / time prediction** | Yandex Go, Yandex Eats, Samokat |
| 📈 **Demand forecasting** | X5, Wildberries, Ozon |
| 🎨 **Image generation** | Sber Kandinsky, Yandex Shedevrum |
| 👀 **Detection / face ID** | Yandex, VK, banks |

---

## 📚 Resources

| Resource | Level |
|---|:---:|
| 🥇 "Machine Learning System Design Interview" — Ali Aminian, Alex Xu | ⭐⭐⭐ |
| 🥇 "Machine Learning System Design" — Valerii Babushkin, Arseny Kravchenko (Manning, RU translation exists) | ⭐⭐⭐ |
| 🥇 [karpov.courses — ML System Design](https://karpov.courses/ml-system-design) | ⭐⭐⭐ |
| 📘 "Designing ML Systems" — Chip Huyen | ⭐⭐⭐ |
| 📚 [Eugene Yan — applied-ml](https://github.com/eugeneyan/applied-ml) — FAANG cases | ⭐⭐⭐ |
| 🎥 Yandex ML Trainings recordings | ⭐⭐ |

---

## ✅ What you should be able to do

- Design a **recommendation system** for a marketplace in 60 minutes.
- Explain why **two-tower** is almost always the first candidate for retrieval.
- Compare **online learning vs batch retraining** for a given case.
- Calculate an end-to-end **latency budget**: DB → feature → model → response.

---

<!-- nav -->
← Back: [⚙️ 7. MLOps & Production](07_mlops.md) · [Contents](../../README.md) · Next: [💼 9. Career in the Russian Market](09_career.md) →
