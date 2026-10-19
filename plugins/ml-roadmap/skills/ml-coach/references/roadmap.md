# Roadmap sections

Source: https://github.com/vincere-mori/ml-engineer-roadmap

Files live in `docs/ru/` and `docs/en/` with the same names. Raw URL pattern:
`https://raw.githubusercontent.com/vincere-mori/ml-engineer-roadmap/main/docs/<ru|en>/<file>`

| # | Section | File | Core of the section | Typical time |
|---|---|---|---|---|
| 1 | Foundations | `01_foundations.md` | Python beyond basics (OOP, generators, typing, asyncio, GIL, pytest), algorithms and Big-O, Linux, Git, uv/ruff | 1-2 months |
| 2 | Math | `02_math.md` | Linear algebra (SVD, PCA), calculus and chain rule, probability and statistics, hypothesis tests, A/B tests, optimization | in parallel |
| 3 | Data | `03_data.md` | Advanced SQL (window functions, EXPLAIN), Pandas/Polars/DuckDB, Spark, Airflow, Kafka, ClickHouse | 1-2 months |
| 4 | Classical ML | `04_classical_ml.md` | Linear models, trees, gradient boosting (CatBoost!), metrics, validation, leakage, recsys basics | 2-3 months |
| 5 | Deep Learning | `05_deep_learning.md` | Backprop, optimizers, normalization, CNN, Transformer, PyTorch, mixed precision, DDP | 2-3 months |
| 6 | Modern AI | `06_modern_ai.md` | Transformers, LLM training and inference, LoRA, RAG, evals, agents and MCP, Russian LLMs | 2-3 months |
| 7 | MLOps | `07_mlops.md` | Docker, k8s, MLflow, DVC, serving (FastAPI, Triton, vLLM), CI/CD, monitoring and drift | 2 months |
| 8 | ML System Design | `08_system_design.md` | Interview framework, typical cases: recommendations, search, antifraud, RAG, ETA, demand | 1 month |
| 9 | Career | `09_career.md` | Internships, job boards, resume, interview stages, negotiation | ongoing |
| 10 | Projects | `10_projects.md` | What makes a pet project strong, project ideas by level, README template | ongoing |
| 11 | Resources | `11_resources.md` | Courses, books (with legal free versions), channels, conferences | - |

## Rough level expectations

- **Intern**: sections 1, 2, 4 at level 2; knows what 5 and 6 are about.
- **Junior**: 1, 2, 3, 4 at level 2+, 5 at level 2, one deployed project, basic 7.
- **Middle**: 4, 5 at level 3, 6 or a specialization at level 2-3, 7 at level 2-3, can lead a system design interview (8) end to end.
- **Senior**: system design at level 3 with real production trade-offs, deep in one specialization, owns metrics and business impact.
