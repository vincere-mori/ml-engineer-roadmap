# ⚙️ 7. MLOps & Production

> Russian version: [07_mlops.md](../ru/07_mlops.md)

> The main difference between an ML Engineer and a Data Scientist is the ability to bring a model **to production** and support it there. This is what senior salaries pay for.

---

## 🐳 Containerization

- [ ] **Docker**: Dockerfile, multi-stage build, slim images
- [ ] docker-compose
- [ ] **Kubernetes** (minimum): pod, deployment, service, ingress, configmap
- [ ] Helm charts (overview)
- [ ] GPU in containers (`nvidia-container-toolkit`)

---

## 📦 Versioning

- [ ] **Git** for code
- [ ] **DVC** / **LakeFS** for data
- [ ] **MLflow Model Registry** / **Weights & Biases Artifacts** for models
- [ ] Model Cards

---

## 🔬 Experiments

- [ ] **MLflow Tracking** — runs, metrics, artifacts
- [ ] **Weights & Biases** — newer, more convenient
- [ ] **ClearML** — open source, self-hostable (useful when SaaS is unavailable)
- [ ] Hydra / OmegaConf — experiment configs

---

## 🚀 Serving (Inference)

| Approach | When to use |
|---|---|
| **FastAPI + Uvicorn** | simple models, REST/JSON |
| **gRPC** | low latency, binary data |
| **Triton Inference Server** | production GPU, multiple models |
| **Ray Serve** | scaling, autoscaling |
| **vLLM / SGLang** | LLM inference |
| **KServe / BentoML** | serving in k8s / model packaging |
| **ONNX Runtime / TensorRT** | hardware optimization |

- [ ] Request batching
- [ ] Caching (Redis)
- [ ] A/B testing models in production
- [ ] Canary / shadow deployment

---

## 🔄 CI/CD for ML

- [ ] **GitHub Actions** / **GitLab CI** — main options in Russia
- [ ] Pre-commit hooks, lint, tests
- [ ] CI: lint → tests → train → eval → deploy
- [ ] **CT (Continuous Training)** — retraining by schedule/trigger
- [ ] Feature stores: **Feast**

---

## 📊 Monitoring

- [ ] **Prometheus + Grafana** — service metrics
- [ ] **Sentry** — errors
- [ ] ML-specific metrics:
  - latency, throughput, RPS
  - data drift, concept drift
  - prediction distribution
- [ ] **Evidently AI** — ML monitoring, open source
- [ ] LLM monitoring: tracing, token cost, answer quality (Langfuse, Phoenix)
- [ ] Alerting

---

## 🏗️ Platforms you may see in Russia

- **Yandex DataSphere** + **Yandex Cloud ML** — Yandex
- **Cloud.ru / SberCloud** — Sber
- **VK Cloud** — VK
- **Selectel ML platform**
- Internal platforms (T-Bank, Avito, X5)

---

## 📚 Resources

| Resource | Level |
|---|:---:|
| 🥇 [Made With ML — MLOps course](https://madewithml.com/) | ⭐⭐⭐ |
| 🎥 [karpov.courses — MLOps](https://karpov.courses/mlops) | ⭐⭐ |
| 📘 "Designing Machine Learning Systems" — Chip Huyen | ⭐⭐⭐ |
| 📘 "Machine Learning Engineering" — Andriy Burkov | ⭐⭐ |
| 🎥 [MLOps Community](https://mlops.community/) | ⭐⭐ |
| 📚 [Awesome MLOps](https://github.com/visenger/awesome-mlops) | — |

---

## ✅ Checkpoint project

**End-to-end ML system:**
1. Train a model (CatBoost / PyTorch)
2. Log experiments in MLflow
3. Version data with DVC
4. Wrap it in Docker + FastAPI
5. CI/CD through GitHub Actions
6. Deploy to k8s (minikube is fine)
7. Prometheus + Grafana dashboard
8. Evidently for drift monitoring
9. README with an architecture diagram

→ This is a **very strong pet project** for your resume.
