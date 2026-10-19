# 🤖 4. Classical ML

> [📋 Contents](../../README.en.md) · [🇷🇺 Русский](../ru/04_classical_ml.md)

> The base of everything. In Russian interviews, classical ML is asked **very deeply**, especially boosting, because **CatBoost** was made at Yandex and is used everywhere.

---

## 🧠 Algorithms (must-know)

### Supervised
- [ ] **Linear regression** — formula derivation, regularization (Ridge, Lasso, ElasticNet)
- [ ] **Logistic regression** — probabilistic interpretation, log-loss
- [ ] **kNN** — metrics, kd-tree
- [ ] **Naive Bayes**
- [ ] **SVM** — kernel trick, soft margin
- [ ] **Decision Trees** — criteria (Gini, entropy, MSE)
- [ ] **Random Forest** — bagging, OOB
- [ ] **Gradient Boosting** — theory, training scheme
  - **XGBoost**
  - **LightGBM**
  - **CatBoost** ← mandatory for the Russian market

### Unsupervised
- [ ] K-Means, K-Means++, MiniBatch
- [ ] Hierarchical clustering
- [ ] DBSCAN, HDBSCAN
- [ ] PCA, t-SNE, UMAP
- [ ] Anomaly detection (Isolation Forest, LOF)

### Recommender Systems
- [ ] Content-based, collaborative filtering
- [ ] Matrix Factorization (ALS, SVD)
- [ ] Implicit / LightFM
- [ ] Two-tower models (introduction)

---

## 📊 Metrics

| Task | Metrics |
|---|---|
| Binary classification | Accuracy, Precision, Recall, F1, ROC-AUC, PR-AUC, log-loss |
| Multiclass | macro/micro/weighted F1 |
| Regression | MSE, RMSE, MAE, MAPE, R² |
| Ranking | NDCG, MAP, MRR, Hit@K |
| Clustering | Silhouette, Davies-Bouldin, ARI |

---

## 🛠️ Technologies

- [ ] **scikit-learn** — Pipeline, ColumnTransformer, GridSearch
- [ ] **CatBoost** ← must know: categorical features, GPU
- [ ] **XGBoost / LightGBM**
- [ ] **Optuna** — hyperparameter tuning
- [ ] **SHAP / LIME** — interpretability
- [ ] **MLflow** (model registry)
- [ ] **Feature engineering**: target/mean encoding, datetime features

---

## 🧪 Validation

- [ ] Train / val / test split, holdout
- [ ] K-Fold, Stratified, GroupKFold, TimeSeriesSplit
- [ ] Data leakage — how to catch it
- [ ] Imbalanced classes (SMOTE, class weights)

---

## 📚 Resources

| Resource | Level |
|---|:---:|
| 🥇 [Yandex School of Data Analysis ML Handbook](https://education.yandex.ru/handbook/ml) — **main Russian-language book** | ⭐⭐⭐ |
| 🥇 [ODS course mlcourse.ai](https://mlcourse.ai) by Yury Kashnitsky | ⭐⭐ |
| 📘 "Hands-On ML" — Aurélien Géron | ⭐⭐ |
| 🎥 [karpov.courses — Simulator ML](https://karpov.courses/simulator-ml) | ⭐⭐ |
| 🎥 [DLS MIPT — Classical ML](https://dls.samcs.ru/) | ⭐⭐ |
| 🏆 [Kaggle Learn](https://www.kaggle.com/learn) | ⭐ |

---

## ✅ Checkpoint projects

1. **Kaggle competition** — get a Bronze medal (Top 10%) in any tabular competition.
2. **Own project**: for example customer churn prediction / credit scoring / demand forecasting. Full pipeline: EDA → features → CatBoost → SHAP → REST API.

---

<!-- nav -->
← Back: [🗄️ 3. Data Engineering for ML](03_data.md) · [Contents](../../README.en.md) · Next: [🧠 5. Deep Learning](05_deep_learning.md) →
