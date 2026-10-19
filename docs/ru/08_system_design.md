# 🏗️ 8. ML System Design

> English version: [08_system_design.md](../en/08_system_design.md)

> **Секция собеседования**, которая чаще всего отделяет Junior от Middle, а Middle от Senior. В Yandex/T-Bank/Avito — обязательная.

---

## 🧩 Фреймворк ответа

1. **Уточни задачу** (clarification): какие метрики бизнеса/ML, нагрузка, SLA, ограничения
2. **Метрики**: бизнес → продуктовые → ML offline → ML online
3. **Данные**: источники, объём, разметка, лейблинг, GDPR/152-ФЗ
4. **Baseline → итерации**: от простого к сложному
5. **Фичи**: feature engineering, feature store
6. **Модель**: кандидаты, выбор, валидация
7. **Inference**: latency, batching, caching, GPU/CPU
8. **Deployment**: A/B, canary, shadow
9. **Мониторинг**: метрики, drift, алерты, retraining
10. **Trade-offs**: что сэкономили, чем пожертвовали

---

## 🎯 Типовые кейсы (надо разобрать!)

| Кейс | Где спрашивают |
|---|---|
| 📺 **Рекомендации видео/товаров** | Yandex (Кинопоиск), VK Clips, Wildberries, Ozon |
| 🔎 **Поиск / ранжирование** | Yandex Search, Avito, Wildberries |
| 💳 **Антифрод / скоринг** | T-Bank, Sber, Альфа |
| 📨 **Спам / модерация** | VK, Avito, Yandex Mail |
| 💬 **Чат-бот / RAG** | Sber GigaChat, Yandex, T-Bank |
| 🚗 **ETA / прогноз времени** | Yandex Go, Яндекс Еда, Самокат |
| 📈 **Прогноз спроса** | X5, Wildberries, Ozon |
| 🎨 **Генерация изображений** | Sber Kandinsky, Yandex Шедеврум |
| 👀 **Detection / face ID** | Yandex, VK, банки |

---

## 📚 Ресурсы

| Ресурс | Уровень |
|---|:---:|
| 🥇 «Machine Learning System Design Interview» — Ali Aminian, Alex Xu | ⭐⭐⭐ |
| 🥇 «Machine Learning System Design» — Валерий Бабушкин, Арсений Кравченко (RU: «Машинное обучение. Проектирование систем от идеи до реализации») | ⭐⭐⭐ |
| 🥇 [karpov.courses — ML System Design](https://karpov.courses/ml-system-design) | ⭐⭐⭐ |
| 📘 «Designing ML Systems» — Chip Huyen | ⭐⭐⭐ |
| 📚 [Eugene Yan — applied-ml](https://github.com/eugeneyan/applied-ml) — кейсы from FAANG | ⭐⭐⭐ |
| 🎥 Записи ML Trainings от Yandex | ⭐⭐ |

---

## ✅ Что должен уметь

- За 60 минут спроектировать **рекомендательную систему** для маркетплейса.
- Объяснить, почему **two-tower** — почти всегда первый кандидат для retrieval.
- Сравнить **online learning vs batch retraining** под кейс.
- Рассчитать **бюджет latency** end-to-end (DB → feature → model → response).

---

<!-- nav -->
← Назад: [⚙️ 7. MLOps & Production](07_mlops.md) · [Оглавление](../../README.md) · Далее: [💼 9. Карьера на российском рынке](09_career.md) →
