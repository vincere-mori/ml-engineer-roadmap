# Question bank

Levels: **J** = Junior, **M** = Middle, **S** = Senior. "Key points" is what a strong answer covers; it is not a script. Accept other correct reasoning. Use these as a base and vary wording; you may ask related questions of the same depth.

## 1. Foundations (Python, CS)

- **J** What is the difference between a list and a tuple, and why can a tuple be a dict key while a list cannot?
  Key points: mutability; dict keys must be hashable; a tuple is hashable only if all its elements are.
- **J** What does a generator give you compared to returning a list?
  Key points: lazy evaluation, memory, `yield`, can be consumed once, useful for streaming data / batches.
- **J** Explain the mutable default argument bug.
  Key points: default evaluated once at def time; shared between calls; fix with `None`.
- **M** What is the GIL and when do threads still help in Python? When do you use processes?
  Key points: one thread executes bytecode at a time; I/O-bound work releases GIL; NumPy/PyTorch release GIL in C code; CPU-bound pure Python needs multiprocessing; DataLoader workers are processes.
- **M** How does a decorator with arguments work? Why `functools.wraps`?
  Key points: three levels of functions; wraps keeps name/docstring/signature.
- **M** asyncio: what happens if you call a blocking function inside a coroutine in a FastAPI endpoint?
  Key points: blocks the event loop, all requests stall; use sync endpoint (threadpool), `run_in_executor`, or async client.
- **J** Big-O of lookup in list vs set vs dict; how is dict implemented?
  Key points: O(n) vs O(1) average; hash table; collisions; worst case.
- **M** Find top-K frequent elements in a stream that does not fit in memory.
  Key points: heap of size K for exact on counts; Count-Min Sketch / Misra-Gries for approximate; trade-offs.

## 2. Math and statistics

- **J** What is the geometric meaning of eigenvectors? How are they related to PCA?
  Key points: directions only scaled by the matrix; PCA = eigenvectors of covariance matrix = right singular vectors of centered data; variance explained.
- **J** Derive the closed-form solution of linear regression with MSE.
  Key points: w = (XᵀX)⁻¹Xᵀy; gradient set to zero; XᵀX may be singular, then ridge or pseudo-inverse; cost O(d³).
- **J** What is a p-value? What it is not?
  Key points: probability of data this extreme or more given H0; not P(H0 true); depends on sample size.
- **M** Design an A/B test for a new ranking model on a marketplace. How do you pick the sample size?
  Key points: metric and unit of randomization; MDE, alpha, power; variance of metric; duration and weekly seasonality; peeking problem; ratio metrics need delta method or bootstrap; network effects.
- **M** MLE vs MAP. How does L2 regularization relate to MAP?
  Key points: MAP adds a prior; Gaussian prior on weights gives L2, Laplace gives L1.
- **M** Why does the CLT matter for A/B tests, and when does it fail you?
  Key points: sample means approx normal; heavy tails, small samples, ratio metrics, dependent observations.
- **S** You have many metrics and many variants in experiments. What goes wrong and what do you do?
  Key points: multiple comparisons; Bonferroni / Holm / FDR; primary vs guardrail metrics; pre-registration; CUPED for variance reduction.

## 3. Data (SQL, pipelines)

- **J** Difference between `WHERE` and `HAVING`; `ROW_NUMBER` vs `RANK` vs `DENSE_RANK`.
  Key points: filter before vs after aggregation; ties behaviour.
- **J** Write a query: for each user, the time since their previous order.
  Key points: `LAG(order_ts) OVER (PARTITION BY user_id ORDER BY order_ts)`.
- **M** A query got slow after the table grew 10x. How do you investigate?
  Key points: EXPLAIN / EXPLAIN ANALYZE; indexes and selectivity; seq scan vs index scan; partitioning; stats; join order.
- **M** Why ClickHouse for analytics and not Postgres? When is it a bad choice?
  Key points: column storage, compression, vectorized execution; bad for point updates/deletes, OLTP, many small transactions.
- **M** How do you build point-in-time correct features for training?
  Key points: features as of prediction time; event timestamps; as-of joins; avoiding future data; feature store offline/online consistency.
- **S** Online features for real-time inference: architecture and failure modes.
  Key points: streaming (Kafka, Flink), online store (Redis etc.), training-serving skew, freshness SLA, backfills, fallback defaults.

## 4. Classical ML

- **J** Bias-variance trade-off with an example of each failure.
  Key points: underfit vs overfit; model complexity; regularization; more data reduces variance.
- **J** Precision, recall, F1, ROC-AUC, PR-AUC. Which one for fraud with 0.1% positives?
  Key points: definitions; ROC-AUC can look great on imbalanced data; PR-AUC or recall at fixed precision; business costs.
- **J** How does a decision tree choose a split? Why are single trees unstable?
  Key points: impurity decrease (Gini, entropy, MSE); greedy; high variance.
- **M** Random forest vs gradient boosting: how they reduce error, which hyperparameters matter.
  Key points: bagging reduces variance, boosting reduces bias; RF: n_estimators, max_features; GB: learning rate, n_estimators, depth, early stopping.
- **M** What is special about CatBoost?
  Key points: ordered target statistics for categorical features (fights target leakage); ordered boosting; symmetric (oblivious) trees, fast inference.
- **M** Give three examples of data leakage and how to catch them.
  Key points: target encoding without folds; scaler/imputer fit before split; random split on time series; duplicates across train/test; features computed after the event; suspiciously high scores, feature importance check, adversarial validation.
- **M** Your offline AUC improved, but the A/B test shows no effect. Possible reasons?
  Key points: offline metric not aligned with business metric; leakage; distribution shift; training-serving skew; position bias / feedback loops; underpowered test.
- **S** How would you validate a model for demand forecasting across thousands of SKUs?
  Key points: time-based backtesting with rolling origin; group-aware splits; metrics like WAPE / MASE; hierarchy; cold start; baseline (seasonal naive).
- **M** How does ALS for implicit feedback work, and how do you evaluate a recommender offline?
  Key points: matrix factorization, alternating least squares, confidence weights; time split; Recall@K, NDCG@K; popularity baseline; coverage.

## 5. Deep Learning

- **J** Walk through backprop for a 2-layer MLP.
  Key points: forward pass caches; chain rule; gradient w.r.t. weights and inputs; shapes.
- **J** Why ReLU over sigmoid in hidden layers?
  Key points: vanishing gradients in saturated sigmoid; cheap; dead ReLU issue.
- **M** BatchNorm vs LayerNorm. Why do Transformers use LayerNorm (often RMSNorm)?
  Key points: normalize over batch vs features; batch-size dependence; sequence lengths; pre-norm stabilizes training.
- **M** Adam vs AdamW. What does weight decay do differently?
  Key points: decoupled weight decay; L2 in Adam gets scaled by adaptive LR.
- **M** Training loss is NaN after a few hundred steps. Debug plan.
  Key points: LR too high, warmup; fp16 overflow, use bf16 / loss scaling; bad data; log(0); gradient clipping; overfit a single batch first.
- **M** What do mixed precision and `torch.compile` give you, and what are the pitfalls?
  Key points: speed and memory with bf16/fp16; numerical issues; compile graph breaks, recompilation with dynamic shapes.
- **S** How does DDP work? When do you need FSDP / ZeRO instead?
  Key points: each GPU full model copy, all-reduce gradients; model does not fit on one GPU → shard params/grads/optimizer states; communication overhead.

## 6. Modern AI (NLP, LLM, RAG)

- **J** Explain self-attention. Why divide by √d?
  Key points: Q, K, V; softmax(QKᵀ/√d)V; large dot products saturate softmax.
- **J** BPE tokenization: how it works and why it matters for Russian text.
  Key points: merges frequent pairs; Russian often takes more tokens per word in English-centric tokenizers → cost and context.
- **M** What is the KV cache and how does it affect memory?
  Key points: cache K and V of previous tokens; memory grows with layers × heads × seq_len × batch; GQA/MQA reduce it; PagedAttention in vLLM.
- **M** LoRA: what is trained, why it works, how to choose rank.
  Key points: low-rank update to frozen weights; few parameters; QLoRA with 4-bit base; rank/alpha trade-off; which layers.
- **M** Build a RAG over company documents in Russian. Walk through the pipeline and how you evaluate it.
  Key points: chunking strategy, multilingual/Russian embeddings (compare on ruMTEB), hybrid BM25 + dense, reranker, prompt with citations; eval retrieval (recall@k) and generation (faithfulness, answer correctness) on a golden set; LLM-as-judge with calibration.
- **M** SFT vs RLHF vs DPO. What does each need in data?
  Key points: demonstrations; preference pairs + reward model + PPO; DPO optimizes on pairs directly without reward model.
- **M** How do you reduce LLM hallucinations in a product?
  Key points: grounding via RAG, citations, refusing when context lacks answer, constrained/structured output, evals, temperature.
- **S** You serve an 8B model and p99 latency is too high under load. Options?
  Key points: continuous batching (vLLM/SGLang), quantization (AWQ, FP8), speculative decoding, prefix caching, smaller model / distillation, limit max tokens, horizontal scaling; measure TTFT vs TPOT separately.
- **S** What changed with reasoning models and RL on verifiable rewards?
  Key points: models trained to produce long chains of thought; GRPO / RLVR on math and code with automatic checking; test-time compute trade-off between cost/latency and quality.
- **M** What is MCP and how does tool calling work under the hood?
  Key points: model outputs a structured call, runtime executes, result goes back to context; MCP standardizes how tools/resources are exposed to agents; security risks like prompt injection.

## 7. MLOps

- **J** Why a multi-stage Docker build? How do you keep an ML image small?
  Key points: build deps separate from runtime; slim base; no cache dirs; CPU vs CUDA images.
- **J** What do you log in MLflow (or analogue) for an experiment?
  Key points: params, metrics, artifacts, code version, data version, environment.
- **M** How do you detect data drift and concept drift? What do you do when it alerts?
  Key points: feature distribution tests (PSI, KS), prediction distribution; concept drift needs labels or proxies; investigate before retraining; retrain triggers.
- **M** Canary vs shadow deployment vs A/B test.
  Key points: small share of real traffic; mirrored traffic without affecting users; statistically measured comparison.
- **M** What is training-serving skew and how do you prevent it?
  Key points: different feature code paths; shared feature definitions / feature store; logging served features; consistency checks.
- **S** Design CI/CD for a model that retrains weekly.
  Key points: data validation, training pipeline, evaluation gates vs current prod model, registry, staged rollout, rollback, monitoring, reproducibility.

## 8. ML System Design

Full cases with rubrics are in [interview.md](interview.md). Short warm-up questions:

- **M** Why are two-tower models the default for candidate retrieval?
  Key points: precompute item embeddings, ANN search, scale to millions; ranking stage is heavier.
- **M** How do you build an end-to-end latency budget?
  Key points: per-stage budget (network, feature fetch, retrieval, ranking, post-processing); p99 not mean; caching.
- **S** Online learning vs periodic batch retraining: when each?
  Key points: freshness needs, stability, feedback loops, infra cost.
