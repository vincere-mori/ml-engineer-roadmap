# 🎯 10. Pet-проекты и портфолио

> English version: [10_projects.md](../en/10_projects.md)

> 2–3 **сильных** проекта на GitHub дают больше оффера, чем 10 туториалов из YouTube. Качество > количество.

---

## 🏆 Что делает проект «сильным»

- ✅ **Реальная задача**, а не туториал «MNIST classification»
- ✅ Полный цикл: **данные → модель → деплой → мониторинг**
- ✅ Чистый код: типизация, тесты, lint, CI
- ✅ Документация: **README с архитектурной схемой**
- ✅ Метрики и сравнение с baseline
- ✅ Демо: видео / Telegram-бот / hosted сервис
- ✅ **Воспроизводимость** (`docker-compose up`)

---

## 💡 Идеи проектов (от джуна к мидлу)

### 🟢 Для старта (1–2 за этап Classical ML)
1. **Прогноз цен на квартиры в твоём городе** — парсинг ЦИАН/Авито → CatBoost → SHAP → FastAPI
2. **Classifier для резюме** — определять грейд по тексту вакансии (hh.ru API)
3. **Прогноз оттока** на open dataset → MLflow + Airflow для ретрейна

### 🟡 Средний уровень (Deep Learning)
4. **CV: классификация / детекция** на своём датасете (например, сорта растений, дорожные знаки)
5. **NLP: классификация отзывов** на русском с fine-tune RuBERT
6. **Свой nanoGPT** на корпусе русской классики, с записью процесса в README

### 🔴 Уровень «возьмут на мидла»
7. **🔥 RAG-бот по своей доменной базе** — Qdrant + GigaChat/YandexGPT + Telegram
8. **🔥 Recommender** для аниме/фильмов/книг — two-tower + ANN (FAISS) + A/B симуляция
9. **🔥 End-to-end MLOps платформа** — модель + DVC + MLflow + k8s + Prometheus + Evidently
10. **🔥 Fine-tune открытой LLM (Qwen3 / T-Pro / GigaChat 3) через LoRA** под конкретную задачу + vLLM serving + свой eval-набор
11. **🔥 Агент с MCP-инструментами** — например, ассистент по своей БД или API, с трейсингом в Langfuse и оценкой качества

### 🤖 Robotics + ML (если интересна область)
12. **RL агент** для манипулятора в симуляторе (Isaac Sim / MuJoCo)
13. **CV для робота**: детекция + трекинг + grasp prediction
14. **VLA (Vision-Language-Action)** — дообучить открытую VLA (OpenVLA, π0 / LeRobot) в симуляторе

---

## 📁 Шаблон README проекта

```markdown
# Project Name

> One-liner о проекте

## 🎯 Задача и мотивация
…

## 🏗️ Архитектура
[архитектурная схема — mermaid или картинка]

## 📊 Результаты
| Метрика | Baseline | Моя модель |
|---|:---:|:---:|
| F1 | 0.72 | **0.83** |
| Latency p99 | 220 ms | **45 ms** |

## 🚀 Запуск
```bash
docker-compose up
```

## 🧰 Стек
Python, PyTorch, FastAPI, Docker, …

## 📚 Что использовалось
- датасет: …
- модель: …
- ссылки на статьи: …
```

---

## 🏆 Kaggle / Соревнования

- 🥉 **Bronze** в табличном — реалистичная цель за 2–3 месяца
- 🥈 Silver — уже сильный сигнал для мидла
- РФ-аналоги: **AI Journey Contest** (Sber), **Yandex Cup** (ML-трек), **DataFest** соревнования

---

## 🌟 GitHub-профиль

- [ ] Pinned 3–6 лучших репо
- [ ] Заполненный bio (ссылка на CV/Telegram)
- [ ] Custom README на профиле (`username/username` репо)
- [ ] Контрибьюты (хотя бы issues / docs) в open source — **большой плюс**
  - PyTorch, Hugging Face, vLLM, Qdrant, CatBoost, ClearML
