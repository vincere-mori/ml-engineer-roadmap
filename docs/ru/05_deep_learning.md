# 🧠 5. Deep Learning

> [📋 Оглавление](../../README.md) · [🇬🇧 English](../en/05_deep_learning.md)

> В РФ де-факто стандарт — **PyTorch**. TensorFlow тоже встречается, но реже.

---

## 🎯 Теория

- [ ] Полносвязная сеть, прямой/обратный проход
- [ ] **Backpropagation** — вывести руками
- [ ] Функции активации: ReLU, GELU, SiLU, sigmoid, tanh, softmax
- [ ] Loss-функции: MSE, BCE, CrossEntropy, focal, contrastive
- [ ] Оптимизаторы: SGD, Momentum, Adam, AdamW, Lion
- [ ] Регуляризация: dropout, batch/layer norm, weight decay, label smoothing
- [ ] Инициализация весов (Xavier, He)
- [ ] Vanishing / exploding gradients

---

## 🏗️ Архитектуры

### Computer Vision
- [ ] CNN: свёртки, пулинг, receptive field
- [ ] LeNet → AlexNet → VGG → ResNet → EfficientNet
- [ ] Detection: YOLO, Faster R-CNN, DETR
- [ ] Segmentation: U-Net, Mask R-CNN
- [ ] Vision Transformer (ViT), Swin

### Sequences
- [ ] RNN, LSTM, GRU (для исторического контекста)
- [ ] Seq2Seq, Attention
- [ ] **Transformer** ← главное (см. след. раздел)

### Generative
- [ ] Autoencoder, VAE
- [ ] GAN, WGAN, StyleGAN
- [ ] Diffusion (DDPM, Stable Diffusion, Kandinsky от Сбера)

---

## 🛠️ PyTorch стек

- [ ] **PyTorch** — `nn.Module`, autograd, custom datasets, DataLoader
- [ ] **PyTorch Lightning** — для чистого кода
- [ ] **Hugging Face Transformers / Datasets / Accelerate**
- [ ] **timm** — pretrained CV модели
- [ ] **Albumentations** — аугментации (оригинальный репозиторий в архиве с 2025, развитие в AlbumentationsX под AGPL; альтернатива `torchvision.transforms.v2`)
- [ ] **Weights & Biases** / **TensorBoard** — логирование
- [ ] Mixed precision (`torch.amp`), `torch.compile`
- [ ] Distributed training (DDP)
- [ ] Профилирование GPU

---

## 📚 Ресурсы

| Ресурс | Уровень |
|---|:---:|
| 🥇 [Deep Learning School МФТИ](https://dls.samcs.ru/) — **топ на русском** | ⭐⭐ |
| 🥇 [ШАД — Deep Learning Handbook](https://education.yandex.ru/handbook/ml) | ⭐⭐⭐ |
| 🎥 [Stanford CS231n](http://cs231n.stanford.edu/) — CV | ⭐⭐⭐ |
| 🎥 [Stanford CS224n](https://web.stanford.edu/class/cs224n/) — NLP | ⭐⭐⭐ |
| 📘 «Deep Learning» — Goodfellow ([бесплатно онлайн](https://www.deeplearningbook.org/), RU: «Глубокое обучение») | ⭐⭐⭐ |
| 📘 «Deep Learning: Foundations and Concepts» — Bishop, 2024 ([бесплатно онлайн](https://www.bishopbook.com/)) | ⭐⭐⭐ |
| 📘 [«Dive into Deep Learning»](https://d2l.ai/) — бесплатно, с кодом на PyTorch | ⭐⭐ |
| 🎥 [karpov.courses — DL](https://karpov.courses/) | ⭐⭐ |
| 🎥 Andrej Karpathy — Neural Networks: Zero to Hero | ⭐⭐⭐ |

---

## ✅ Контрольные проекты

1. С нуля написать **MLP + backprop без autograd** (numpy).
2. Обучить **ResNet-like модель** на CIFAR-100, выжать максимум через аугментации.
3. **Fine-tune** предобученной модели под свою задачу + деплой через FastAPI.

---

<!-- nav -->
← Назад: [🤖 4. Classical ML](04_classical_ml.md) · [Оглавление](../../README.md) · Далее: [💬 6. Modern AI — NLP, LLM, RAG](06_modern_ai.md) →
