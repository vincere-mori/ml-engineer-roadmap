# 🐍 1. Foundations — Python, алгоритмы, CS

> [📋 Оглавление](../../README.md) · [🇬🇧 English](../en/01_foundations.md)

> **Цель этапа:** уверенно писать продакшен-код на Python, понимать как работает компьютер, проходить алгоритмические секции собеседований.

---

## 🎯 Что должен знать ML Engineer

### Python (Advanced)
- [ ] Типы данных, mutable/immutable, copy/deepcopy
- [ ] ООП: классы, наследование, миксины, dataclasses, `__slots__`
- [ ] Декораторы, контекстные менеджеры, генераторы, итераторы
- [ ] Типизация (`typing`, `mypy`), `pydantic`
- [ ] Асинхронность: `asyncio`, `async/await`
- [ ] Многопоточность vs многопроцессорность, GIL
- [ ] Тесты: `pytest`, фикстуры, моки, coverage
- [ ] Менеджмент зависимостей: **`uv`** (стандарт де-факто с 2025), `poetry` в легаси-проектах
- [ ] Линтеры/форматтеры: `ruff` (lint + format, заменил black/isort/flake8), `pre-commit`, тайпчекер `mypy` / `pyright`

### Computer Science
- [ ] Структуры данных: list, dict, set, deque, heap, trie
- [ ] Алгоритмы: сортировки, BFS/DFS, DP, two pointers, sliding window
- [ ] Сложность по времени и памяти (Big-O)
- [ ] Базы ОС: процессы, потоки, память, IPC
- [ ] Сети: HTTP/HTTPS, TCP/UDP, REST, gRPC, WebSockets

### Инструменты разработчика
- [ ] Git: ветвление, rebase, conflict resolution, git hooks
- [ ] Linux: bash, grep/sed/awk, systemd, ssh, screen/tmux
- [ ] IDE: PyCharm / VS Code + плагины
- [ ] Docker (введение, глубже — в MLOps)

---

## 📚 Ресурсы

| Тип | Ресурс | Уровень |
|---|---|:---:|
| 📖 Книга | «Fluent Python» Лучано Рамальо (RU: «Python. К вершинам мастерства», 2-е изд.) | ⭐⭐⭐ |
| 🎥 Курс | [Поколение Python (Stepik)](https://stepik.org/course/58852) | ⭐ |
| 🎥 Курс | [Алгоритмы: теория и практика — Computer Science Center](https://stepik.org/course/217) | ⭐⭐ |
| 🎥 Курс | [Яндекс — Тренировки по алгоритмам](https://contest.yandex.ru/tracks/algorithms/) | ⭐⭐⭐ |
| 💻 Практика | [LeetCode](https://leetcode.com) — 100–150 задач Easy/Medium | ⭐⭐ |
| 💻 Практика | [Codeforces](https://codeforces.com) | ⭐⭐ |
| 🎥 Linux | [Курс «Введение в Linux» (Stepik)](https://stepik.org/course/73) | ⭐ |
| 🎥 Git | [Git для начинающих — Хирьянов](https://www.youtube.com/watch?v=zZBiln_2FhM) | ⭐ |

---

## ✅ Контрольный проект

Напиши **CLI-утилиту** на Python, которая:
- парсит CSV/JSON,
- считает простую статистику,
- покрыта тестами `pytest` (≥80% coverage),
- собрана через `uv` (`pyproject.toml` + `uv.lock`),
- имеет `Dockerfile`,
- лежит на GitHub с README + GitHub Actions (lint + tests).

---

<!-- nav -->
[Оглавление](../../README.md) · Далее: [📐 2. Математика для ML](02_math.md) →
