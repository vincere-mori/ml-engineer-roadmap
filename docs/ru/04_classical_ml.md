# 🤖 4. Classical ML

> [📋 Оглавление](../../README.md) · [🇬🇧 English](../en/04_classical_ml.md)

> Основа всего. На собеседованиях в РФ classical ML спрашивают **очень глубоко** — особенно бустинги (потому что **CatBoost** сделан в Yandex и используется везде).

---

## 🧠 Алгоритмы (must-know)

### Supervised
- [ ] **Линейная регрессия** — вывод формулы, регуляризация (Ridge, Lasso, ElasticNet)
- [ ] **Логистическая регрессия** — вероятностная интерпретация, log-loss
- [ ] **kNN** — метрики, kd-tree
- [ ] **Naive Bayes**
- [ ] **SVM** — kernel trick, soft margin
- [ ] **Decision Trees** — критерии (Gini, entropy, MSE)
- [ ] **Random Forest** — bagging, OOB
- [ ] **Gradient Boosting** — теория, схема обучения
  - **XGBoost**
  - **LightGBM**
  - **CatBoost** ← обязательно для РФ-рынка

### Unsupervised
- [ ] K-Means, K-Means++, MiniBatch
- [ ] Иерархическая кластеризация
- [ ] DBSCAN, HDBSCAN
- [ ] PCA, t-SNE, UMAP
- [ ] Anomaly detection (Isolation Forest, LOF)

### Recommender Systems
- [ ] Content-based, collaborative filtering
- [ ] Matrix Factorization (ALS, SVD)
- [ ] Implicit / LightFM
- [ ] Two-tower модели (введение)

---

## 📊 Метрики

| Задача | Метрики |
|---|---|
| Бинарная классификация | Accuracy, Precision, Recall, F1, ROC-AUC, PR-AUC, log-loss |
| Multiclass | macro/micro/weighted F1 |
| Регрессия | MSE, RMSE, MAE, MAPE, R² |
| Ранжирование | NDCG, MAP, MRR, Hit@K |
| Кластеризация | Silhouette, Davies-Bouldin, ARI |

---

## 🛠️ Технологии

- [ ] **scikit-learn** — Pipeline, ColumnTransformer, GridSearch
- [ ] **CatBoost** ← знать обязательно (категориальные фичи, GPU)
- [ ] **XGBoost / LightGBM**
- [ ] **Optuna** — подбор гиперпараметров
- [ ] **SHAP / LIME** — интерпретируемость
- [ ] **MLflow** (регистрация моделей)
- [ ] **Feature engineering**: target/mean encoding, datetime features

---

## 🧪 Валидация

- [ ] Train / val / test split, holdout
- [ ] K-Fold, Stratified, GroupKFold, TimeSeriesSplit
- [ ] Утечки данных (data leakage) — как ловить
- [ ] Несбалансированные классы (SMOTE, class weights)

---

## 📚 Ресурсы

| Ресурс | Уровень |
|---|:---:|
| 🥇 [ШАД ML Handbook (Yandex)](https://education.yandex.ru/handbook/ml) — **главная книга на русском** | ⭐⭐⭐ |
| 🥇 [ODS курс mlcourse.ai](https://mlcourse.ai) (Юрий Кашницкий) | ⭐⭐ |
| 📘 «Hands-On ML» — Aurélien Géron | ⭐⭐ |
| 🎥 [karpov.courses — Simulator ML](https://karpov.courses/simulator-ml) | ⭐⭐ |
| 🎥 [DLS МФТИ — Classical ML](https://dls.samcs.ru/) | ⭐⭐ |
| 🏆 [Kaggle Learn](https://www.kaggle.com/learn) | ⭐ |

---

## ✅ Контрольные проекты

1. **Kaggle competition** — взять Bronze медаль (Top 10%) в любом табличном соревновании.
2. **Свой проект**: например, прогноз оттока клиентов / скоринг кредитных заявок / прогноз спроса. Полный пайплайн: EDA → фичи → CatBoost → SHAP → REST-API.

---

<!-- nav -->
← Назад: [🗄️ 3. Data Engineering для ML](03_data.md) · [Оглавление](../../README.md) · Далее: [🧠 5. Deep Learning](05_deep_learning.md) →
