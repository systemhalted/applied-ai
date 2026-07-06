# Phase 2 — Deep Learning Fundamentals (CS230)

**Modules 18–20 · Primary course: Stanford CS230 Deep Learning · Typical duration: 2–4 months**

*Move from classical ML to neural networks. Build intuition before adding complexity.*

## Course links

- Course page: <https://cs230.stanford.edu/>
- Stanford Online: <https://online.stanford.edu/courses/cs230-deep-learning>
- YouTube lectures (Autumn 2018, Andrew Ng): <https://www.youtube.com/playlist?list=PLoROMvodv4rOABXSygHTsbvUz4G_YQhOb> — note CS230 runs flipped-classroom, so these lectures are strategy and project-craft; the technical depth lives in the deeplearning.ai companion below
- Companion: deeplearning.ai Deep Learning Specialization (Coursera) — CS230 aligns with this. Use Coursera for graded assignments if you want structured practice alongside the Stanford lectures: <https://www.coursera.org/specializations/deep-learning>

## Module 18 — Neural network basics: forward pass, loss, backpropagation

**Topics:**

- CS230 / deeplearning.ai Course 1, Weeks 1–4: Neural Networks and Deep Learning (the build below needs Week 3's shallow-network material — do not stop at Week 2)
- Implement a 2-layer neural net in pure NumPy — forward pass, loss, backward pass, weight update
- Then implement the same network in PyTorch. Compare: what did PyTorch handle automatically?

**Resources:**

- Andrej Karpathy — "The spelled-out intro to neural networks and backpropagation" (YouTube, 2.5 hrs): <https://www.youtube.com/watch?v=VMj-3S1tku0>

**Math checkpoint:** the chain rule in backprop is your math-phase Course 2 work in action. If it feels disconnected, re-read your calculus notes on composite function derivatives.

**▸ Build:** NumPy neural net AND PyTorch neural net. Same architecture, same dataset as Phase 1, documented comparison of results. Before comparing, verify your NumPy backward pass: your gradients should match PyTorch's autograd (or a finite-difference check) on one batch to within ~1e-6 — if they do not, the comparison is meaningless; fix the backprop first. A Markdown explanation of what autograd is doing.

**⚠ Note:** The NumPy implementation is not busywork. It is the only way to know what PyTorch is doing for you — which matters when things break in production.

## Module 19 — Training dynamics: dropout, batch normalization, learning rate

**Topics:**

- CS230 / deeplearning.ai Course 2: Improving Deep Neural Networks — all three weeks
- Weight initialization, dropout, batch normalization, Adam optimizer, learning rate decay
- PyTorch: add `Dropout` and `BatchNorm` layers to your Module 18 network
- Plot training and validation loss curves. Learn to read them diagnostically — this is a skill you will use every time you debug a model, yours or someone else's.

**▸ Build:** Training diagnostic report: loss curves for four configurations (baseline, dropout, batch norm, both) — same seed, same epoch budget across all four, or the comparison is invalid by construction. Written in Markdown. One paragraph of interpretation per configuration — written for a reader who has never trained a neural network.

## Module 20 — CNNs and the structure of deep learning projects

**Topics:**

- CS230 / deeplearning.ai Course 3: Structuring ML Projects (short — about two weeks of material, high value)
- CS230 / deeplearning.ai Course 4, Week 1: Convolutional Neural Networks
- Build a minimal CNN in PyTorch on CIFAR-10
- Compare CNN vs MLP on the same image task — document the result
- **Work in someone else's code:** clone an existing open training repo (Karpathy's [nanoGPT](https://github.com/karpathy/nanoGPT) or a [torchvision reference script](https://github.com/pytorch/vision/tree/main/references/classification)), get it running, and change exactly one thing (a hyperparameter, a layer, a logging line). Most real ML work is reading and extending code you did not write — this is deliberate practice for it.

**Supplement:**

- fast.ai Lesson 1 (free). Shows a practical top-down CNN workflow in 2 hours. Excellent complement to the bottom-up CS230 approach: <https://course.fast.ai/>

**▸ Build:** CNN trained on CIFAR-10, >70% validation accuracy. Training curves, confusion matrix, and a written note on the three most common failure modes you observed. Plus a short log entry on the someone-else's-code exercise: what you had to understand before your one-line change worked.

## Completion gate — written, not felt

Answer these in your learning log as a self-quiz (writing them down is the gate; a feeling of familiarity is not):

1. What is the vanishing gradient problem, and how do batch normalization and skip connections each address it?
2. What does autograd actually compute, and what would you have to write by hand without it?
3. Sketch (in words) a training curve showing overfitting, one showing underfitting, and one showing a learning rate set too high. How do you respond to each?
4. Why does a CNN beat an MLP on images? What assumption is it exploiting?
5. Spaced retrieval: re-answer, cold, two questions of your choice from the Phase 1 gate.

If any answer will not come, rewatch the relevant lecture before choosing a track.

## Choose your specialization track — before Module 21, and commit

One track. Completely. Do not mix with the other until the capstone is done.

- **Track A (NLP / LLMs): [CS224N](4a-nlp.md)** — recommended for most learners right now. LLMs are where the leverage is for platform and integration work.
- **Track B (Computer Vision): [CS231n](4b-vision.md)** — choose this if you work with visual data, document understanding, or image-based workflows.
- If genuinely unsure: choose Track A. CS231n can be a later elective. CS224N skills compound faster for most applied AI use cases.

---

[← Phase 1 — Core ML](2-core-ml.md) · [Curriculum overview](../README.md) · Next: [Track A — NLP →](4a-nlp.md) or [Track B — Vision →](4b-vision.md)
