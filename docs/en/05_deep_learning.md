# 🧠 5. Deep Learning

> [📋 Contents](../../README.en.md) · [🇷🇺 Русский](../ru/05_deep_learning.md)

> In Russia, the de facto standard is **PyTorch**. TensorFlow exists too, but is less common.

---

## 🎯 Theory

- [ ] Fully connected network, forward/backward pass
- [ ] **Backpropagation** — derive it by hand
- [ ] Activation functions: ReLU, GELU, SiLU, sigmoid, tanh, softmax
- [ ] Loss functions: MSE, BCE, CrossEntropy, focal, contrastive
- [ ] Optimizers: SGD, Momentum, Adam, AdamW, Lion
- [ ] Regularization: dropout, batch/layer norm, weight decay, label smoothing
- [ ] Weight initialization (Xavier, He)
- [ ] Vanishing / exploding gradients

---

## 🏗️ Architectures

### Computer Vision
- [ ] CNN: convolutions, pooling, receptive field
- [ ] LeNet → AlexNet → VGG → ResNet → EfficientNet
- [ ] Detection: YOLO, Faster R-CNN, DETR
- [ ] Segmentation: U-Net, Mask R-CNN
- [ ] Vision Transformer (ViT), Swin

### Sequences
- [ ] RNN, LSTM, GRU (for historical context)
- [ ] Seq2Seq, Attention
- [ ] **Transformer** ← main topic; see next section

### Generative
- [ ] Autoencoder, VAE
- [ ] GAN, WGAN, StyleGAN
- [ ] Diffusion (DDPM, Stable Diffusion, Kandinsky by Sber)

---

## 🛠️ PyTorch stack

- [ ] **PyTorch** — `nn.Module`, autograd, custom datasets, DataLoader
- [ ] **PyTorch Lightning** — cleaner code
- [ ] **Hugging Face Transformers / Datasets / Accelerate**
- [ ] **timm** — pretrained CV models
- [ ] **Albumentations** — augmentations (original repo archived in 2025, continued as AlbumentationsX under AGPL; alternative: `torchvision.transforms.v2`)
- [ ] **Weights & Biases** / **TensorBoard** — logging
- [ ] Mixed precision (`torch.amp`), `torch.compile`
- [ ] Distributed training (DDP)
- [ ] GPU profiling

---

## 📚 Resources

| Resource | Level |
|---|:---:|
| 🥇 [Deep Learning School MIPT](https://dls.samcs.ru/) — **top Russian-language course** | ⭐⭐ |
| 🥇 [Yandex School of Data Analysis — Deep Learning Handbook](https://education.yandex.ru/handbook/ml) | ⭐⭐⭐ |
| 🎥 [Stanford CS231n](http://cs231n.stanford.edu/) — CV | ⭐⭐⭐ |
| 🎥 [Stanford CS224n](https://web.stanford.edu/class/cs224n/) — NLP | ⭐⭐⭐ |
| 📘 "Deep Learning" — Goodfellow ([free online](https://www.deeplearningbook.org/)) | ⭐⭐⭐ |
| 📘 "Deep Learning: Foundations and Concepts" — Bishop, 2024 ([free online](https://www.bishopbook.com/)) | ⭐⭐⭐ |
| 📘 ["Dive into Deep Learning"](https://d2l.ai/) — free, PyTorch code | ⭐⭐ |
| 🎥 [karpov.courses — DL](https://karpov.courses/) | ⭐⭐ |
| 🎥 Andrej Karpathy — Neural Networks: Zero to Hero | ⭐⭐⭐ |

---

## ✅ Checkpoint projects

1. Write **MLP + backprop without autograd** from scratch in NumPy.
2. Train a **ResNet-like model** on CIFAR-100 and squeeze performance through augmentations.
3. **Fine-tune** a pretrained model for your own task + deploy through FastAPI.

---

<!-- nav -->
← Back: [🤖 4. Classical ML](04_classical_ml.md) · [Contents](../../README.en.md) · Next: [💬 6. Modern AI — NLP, LLM, RAG](06_modern_ai.md) →
