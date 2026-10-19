# ⚙️ 7. MLOps & Production

> [📋 Оглавление](../../README.md) · [🇬🇧 English](../en/07_mlops.md)

> **Главное отличие** ML Engineer от Data Scientist — умение довести модель **до прода** и поддерживать её там. Именно за это платят senior-зарплаты.

---

## 🐳 Контейнеризация

- [ ] **Docker**: Dockerfile, multi-stage build, slim images
- [ ] docker-compose
- [ ] **Kubernetes** (минимум): pod, deployment, service, ingress, configmap
- [ ] Helm charts (обзорно)
- [ ] GPU в контейнерах (`nvidia-container-toolkit`)

---

## 📦 Версионирование

- [ ] **Git** для кода
- [ ] **DVC** / **lakeFS** для данных
- [ ] **MLflow Model Registry** / **Weights & Biases Artifacts** — для моделей
- [ ] Модельные карточки (Model Cards)

---

## 🔬 Эксперименты

- [ ] **MLflow Tracking** — запуски, метрики, артефакты
- [ ] **Weights & Biases** — современнее, удобнее
- [ ] **ClearML** — open source, можно поднять у себя (актуально, когда SaaS недоступен)
- [ ] Hydra / OmegaConf — конфиги экспериментов

---

## 🚀 Serving (inference)

| Подход | Когда использовать |
|---|---|
| **FastAPI + Uvicorn** | простые модели, REST/JSON |
| **gRPC** | низкая latency, бинарные данные |
| **Triton Inference Server** | продакшен GPU, мульти-модели |
| **Ray Serve** | масштабирование, autoscaling |
| **vLLM / SGLang** | LLM inference |
| **KServe / BentoML** | serving в k8s / упаковка моделей |
| **ONNX Runtime / TensorRT** | оптимизация под железо |

- [ ] Батчинг запросов
- [ ] Caching (Redis)
- [ ] A/B тестирование моделей в проде
- [ ] Canary / shadow deployment

---

## 🔄 CI/CD для ML

- [ ] **GitHub Actions** / **GitLab CI** — основные в РФ
- [ ] Pre-commit hooks, lint, тесты
- [ ] CI: lint → tests → train → eval → deploy
- [ ] **CT (Continuous Training)** — переобучение по расписанию/триггеру
- [ ] Feature stores: **Feast**

---

## 📊 Мониторинг

- [ ] **Prometheus + Grafana** — метрики сервиса
- [ ] **Sentry** — ошибки
- [ ] ML-специфичные метрики:
  - latency, throughput, RPS
  - data drift, concept drift
  - prediction distribution
- [ ] **Evidently AI** — ML-мониторинг (open source)
- [ ] LLM-мониторинг: трейсинг, стоимость токенов, качество ответов (Langfuse, Phoenix)
- [ ] Алертинг

---

## 🏗️ Платформы (что встретишь в РФ)

- **Yandex DataSphere** + **Yandex Cloud ML** — Yandex
- **Cloud.ru / SberCloud** — Sber
- **VK Cloud** — VK
- **Selectel ML platform**
- Внутренние платформы (T-Bank, Avito, X5)

---

## 📚 Ресурсы

| Ресурс | Уровень |
|---|:---:|
| 🥇 [Made With ML — MLOps course](https://madewithml.com/) | ⭐⭐⭐ |
| 🎥 [karpov.courses — MLOps](https://karpov.courses/mlops) | ⭐⭐ |
| 📘 «Designing Machine Learning Systems» — Chip Huyen | ⭐⭐⭐ |
| 📘 «Machine Learning Engineering» — Andriy Burkov | ⭐⭐ |
| 🎥 [MLOps Community](https://mlops.community/) | ⭐⭐ |
| 📚 [Awesome MLOps](https://github.com/visenger/awesome-mlops) | — |

---

## ✅ Контрольный проект

**End-to-end ML система:**
1. Обучи модель (CatBoost / PyTorch)
2. Логируй эксперименты в MLflow
3. Версионируй данные через DVC
4. Заверни в Docker + FastAPI
5. CI/CD через GitHub Actions
6. Деплой в k8s (можно minikube)
7. Prometheus + Grafana дашборд
8. Evidently для drift-мониторинга
9. README с архитектурной схемой

→ Это **сильнейший pet-проект** для резюме.

---

<!-- nav -->
← Назад: [💬 6. Modern AI — NLP, LLM, RAG](06_modern_ai.md) · [Оглавление](../../README.md) · Далее: [🏗️ 8. ML System Design](08_system_design.md) →
