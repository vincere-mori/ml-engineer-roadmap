# 🐍 1. Foundations — Python, algorithms, CS

> [📋 Contents](../../README.en.md) · [🇷🇺 Русский](../ru/01_foundations.md)

> **Stage goal:** write production code in Python confidently, understand how computers work, and pass algorithmic interview rounds.

---

## 🎯 What an ML Engineer should know

### Python (Advanced)
- [ ] Data types, mutable/immutable, copy/deepcopy
- [ ] OOP: classes, inheritance, mixins, dataclasses, `__slots__`
- [ ] Decorators, context managers, generators, iterators
- [ ] Typing (`typing`, `mypy`), `pydantic`
- [ ] Async: `asyncio`, `async/await`
- [ ] Multithreading vs multiprocessing, GIL
- [ ] Tests: `pytest`, fixtures, mocks, coverage
- [ ] Dependency management: **`uv`** (de facto standard since 2025), `poetry` in legacy projects
- [ ] Linters/formatters: `ruff` (lint + format, replaced black/isort/flake8), `pre-commit`, type checker `mypy` / `pyright`

### Computer Science
- [ ] Data structures: list, dict, set, deque, heap, trie
- [ ] Algorithms: sorting, BFS/DFS, DP, two pointers, sliding window
- [ ] Time and memory complexity (Big-O)
- [ ] OS basics: processes, threads, memory, IPC
- [ ] Networking: HTTP/HTTPS, TCP/UDP, REST, gRPC, WebSockets

### Developer tools
- [ ] Git: branching, rebase, conflict resolution, git hooks
- [ ] Linux: bash, grep/sed/awk, systemd, ssh, screen/tmux
- [ ] IDE: PyCharm / VS Code + plugins
- [ ] Docker basics; deeper dive in MLOps

---

## 📚 Resources

| Type | Resource | Level |
|---|---|:---:|
| 📖 Book | "Fluent Python" by Luciano Ramalho, 2nd ed. | ⭐⭐⭐ |
| 🎥 Course | [Generation Python (Stepik)](https://stepik.org/course/58852) | ⭐ |
| 🎥 Course | [Algorithms: Theory and Practice — Computer Science Center](https://stepik.org/course/217) | ⭐⭐ |
| 🎥 Course | [Yandex School of Data Analysis — Algorithms and Data Structures](https://contest.yandex.ru/tracks/algorithms/) | ⭐⭐⭐ |
| 💻 Practice | [LeetCode](https://leetcode.com) — 100–150 Easy/Medium problems | ⭐⭐ |
| 💻 Practice | [Codeforces](https://codeforces.com) | ⭐⭐ |
| 🎥 Linux | [Introduction to Linux (Stepik)](https://stepik.org/course/73) | ⭐ |
| 🎥 Git | [Git for beginners — Khiryanov](https://www.youtube.com/watch?v=zZBiln_2FhM) | ⭐ |

---

## ✅ Checkpoint project

Write a Python **CLI utility** that:
- parses CSV/JSON,
- calculates simple statistics,
- is covered with `pytest` tests (≥80% coverage),
- is packaged with `uv` (`pyproject.toml` + `uv.lock`),
- has a `Dockerfile`,
- is published on GitHub with README + GitHub Actions (lint + tests).

---

<!-- nav -->
[Contents](../../README.en.md) · Next: [📐 2. Math for ML](02_math.md) →
