# 📐 2. Math for ML

> Russian version: [02_math.md](../ru/02_math.md)

> **Goal:** not just "know formulas", but **understand** what happens inside models. Yandex/Sber/T-Bank interviews can go deep on math.

---

## 🧩 Linear Algebra

- [ ] Vectors, matrices, operations
- [ ] Dot product / cross product, norms
- [ ] Rank, determinant, inverse matrix
- [ ] Systems of linear equations, Gaussian elimination
- [ ] Eigenvalues and eigenvectors, SVD, PCA
- [ ] Positive definite matrices

📚 **Resources:**
- [Khan Academy — Linear Algebra](https://www.khanacademy.org/math/linear-algebra)
- [3Blue1Brown — Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) (Russian subtitles)
- [Yandex School of Data Analysis — ML Handbook](https://education.yandex.ru/handbook/ml)
- Kostrikin, "Introduction to Algebra"

---

## 📈 Calculus

- [ ] Derivatives, partial derivatives, gradient
- [ ] Chain rule (the basis of backprop!)
- [ ] Jacobian, Hessian
- [ ] Taylor series
- [ ] Multidimensional optimization, Lagrangian
- [ ] Convexity, convex functions

📚 **Resources:**
- [MIPT — Calculus (Coursera/archive)](https://openedu.ru/)
- 3Blue1Brown — Essence of Calculus

---

## 🎲 Probability and Statistics

> **The most important part** for ML interviews.

- [ ] Probability spaces, conditional probability, Bayes
- [ ] Random variables, distributions (normal, Bernoulli, Poisson, exponential)
- [ ] Expected value, variance, covariance, correlation
- [ ] CLT, law of large numbers
- [ ] Point and interval estimates, MLE, MAP
- [ ] Hypothesis testing: t-test, χ², Mann-Whitney
- [ ] A/B tests: design, power, MDE, bootstrap
- [ ] Causal inference (introduction)

📚 **Resources:**
- [Karpov course — A/B tests](https://karpov.courses/simulator-ab) — gold standard
- [Yandex School of Data Analysis — Probability and Statistics](https://education.yandex.ru/handbook/ml)
- Wasserman, "All of Statistics"
- [Stepik — Fundamentals of Statistics (Anatoly Karpov)](https://stepik.org/course/76)

---

## ⚙️ Optimization

- [ ] Gradient descent (SGD, Momentum, Adam, AdamW)
- [ ] Stochastic GD vs batch GD
- [ ] Learning rate schedules
- [ ] L1/L2 regularization
- [ ] Newton method, quasi-Newton methods
- [ ] Constrained optimization

---

## ✅ What you should be able to do by the end

- Explain **in simple words** what SVD is and why it is used in ML
- **Derive** linear regression through least squares by yourself
- Explain how **backpropagation** works through the chain rule
- Design an **A/B test** for a given product case

---

<!-- nav -->
← Back: [🐍 1. Foundations — Python, algorithms, CS](01_foundations.md) · [Contents](../../README.md) · Next: [🗄️ 3. Data Engineering for ML](03_data.md) →
