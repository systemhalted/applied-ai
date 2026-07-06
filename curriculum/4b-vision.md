# Phase 3, Track B — Computer Vision (CS231n)

**Modules 21–25 · Primary course: Stanford CS231n Deep Learning for Computer Vision · Typical duration: 4–6 months**

*One track. Completely. If you chose [Track A — NLP](4a-nlp.md), skip this file.*

## Course links

- Course page: <https://cs231n.stanford.edu/>
- Course notes: <https://cs231n.github.io/>
- YouTube lectures: <https://www.youtube.com/playlist?list=PLoROMvodv4rOmsNzYBMe0gJY2XS8AQg16> — lecture numbers below follow this 2025 offering; they shift between years, so match by topic if a number looks wrong
- Assignments: from cs231n.github.io. **Required:** Assignment 1 (kNN, softmax, two-layer net, image features — contents shift slightly between years), Assignment 2 (ConvNets), and Assignment 3 (network visualization, transformers/attention — check the current offering's contents). The assignments are the course; the lectures are commentary on them. The assignment notebooks ship with built-in sanity checks and expected values — those, not a notebook that merely runs, are the correctness standard.

## Module 21 — Image classification and CNN architecture

**Topics:**

- CS231n Lectures 1–5: Image Classification, Loss, Backprop, Neural Networks, CNNs
- CS231n Assignment 1 (required)
- PyTorch: build and train a custom CNN from scratch on CIFAR-10 — you built one in Module 20; rebuild it here *without* referring to that notebook, then beat your Module 20 accuracy. Rebuilding from memory is the point.

**Resources:**

- "ImageNet Classification with Deep Convolutional Neural Networks" (Krizhevsky et al., 2012) — the AlexNet paper, 9 pages: <https://papers.nips.cc/paper_files/paper/2012/hash/c399862d3b9d6b76c8436e924a68c45b-Abstract.html>

**▸ Build:** Custom CNN on CIFAR-10 from scratch. Visualize 10 misclassifications with their true label, predicted label, and confidence score. Written analysis: what patterns explain the failures? Assignment 1 completed.

**⚠ Budget note:** the assignment makes this two to three modules of work — plan 2–4 calendar weeks (CS231n assignments run heavier than most). Same for every assignment-bearing module in this track.

## Module 22 — Transfer learning and modern architectures

**Topics:**

- CS231n: the CNN-architectures lecture — match by topic; it covers the AlexNet → VGG → ResNet lineage, which is exactly what you are about to fine-tune
- CS231n Assignment 2 (required)
- torchvision: fine-tune ResNet-18 on a 2-class image dataset relevant to your domain

**Supplement:**

- fast.ai Lessons 1–2 (free). Fast.ai's transfer learning API is the fastest practical path through this material: <https://course.fast.ai/>

**▸ Build:** Fine-tuned ResNet-18 vs training from scratch: same dataset, same training budget, documented comparison. On a small dataset, transfer learning should win decisively — if it does not, something is wrong with your setup; debug before writing the comparison. One paragraph: when would you choose transfer learning vs training from scratch for a real use case? Assignment 2 completed.

## Module 23 — Object detection and segmentation

**Topics:**

- CS231n Lecture 9: Object Detection, Instance Segmentation
- torchvision: run pre-trained Faster R-CNN and Mask R-CNN on your own images
- YOLO quickstart: Ultralytics documentation at <https://docs.ultralytics.com/>

**Supplement (gap):**

- Udemy — "PyTorch for Deep Learning" (Daniel Bourke), detection section. Fills the applied pipeline detail CS231n leaves abstract: <https://www.udemy.com/course/pytorch-for-deep-learning/>

**▸ Build:** Object detection pipeline: Faster R-CNN on 20 images, bounding boxes and confidence scores visualized. Report detections at three confidence thresholds (e.g., 0.3 / 0.5 / 0.9): count the false positives and misses at each across your 20 images, then say which threshold you would ship for a stated use case and why.

## Module 24 — Vision transformers

**Topics:**

- CS231n Lecture 8: Attention and Transformers — the ViT material
- CS231n Assignment 3 (required)
- HuggingFace Transformers: load ViT, run inference, compare to ResNet on your fine-tuning task

**Resources:**

- "An Image is Worth 16x16 Words" (Dosovitskiy et al., 2020) — the ViT paper: <https://arxiv.org/abs/2010.11929>

**▸ Build:** ViT vs ResNet comparison notebook. Same dataset, same training budget. A one-page technical brief: which model would you recommend for a real use case, and what are the trade-offs? Write it for a technically literate reader who is not an ML specialist. Assignment 3 completed.

## Module 25 — Multimodal models: CLIP, SAM, and the vision-language landscape

Modern vision increasingly speaks language. This module covers the models that changed what "computer vision" means.

**Topics:**

- CLIP — contrastive language-image pretraining: read "Learning Transferable Visual Models From Natural Language Supervision" (Radford et al., 2021): <https://arxiv.org/abs/2103.00020>
- Zero-shot classification with CLIP via HuggingFace Transformers — no training, just prompts
- The Segment Anything lineage — promptable segmentation, as read-only survey (no build item; the module is full): the original SAM paper for the concept (Kirillov et al., 2023: <https://arxiv.org/abs/2304.02643>), then skim how SAM 2 added video and SAM 3 added text-prompted concept segmentation: <https://github.com/facebookresearch/sam3>
- Survey the vision-language model landscape: what can current open VLMs do (image captioning, visual QA, document understanding), and what are their failure modes? Document what you find.

**▸ Build:** Zero-shot CLIP classifier on the same dataset as your Module 22 fine-tuned ResNet — same test split, one comparison table. When does zero-shot win, when does fine-tuning win, and what does that imply about when training a custom vision model is still worth it? One page.

**⚠ Note:** The CLIP-vs-fine-tuning question is the practical heart of modern applied vision. Many production vision problems today are solved with zero training at all — knowing when that is true is the skill.

## Completion gate — written, not felt

Answer in your log before starting the capstone:

1. Why does a CNN need orders of magnitude less data than a ViT to train from scratch, and why does pretraining erase that advantage?
2. When would you reach for zero-shot CLIP vs fine-tuning a classifier vs training from scratch? Concrete example of each.
3. What does an object detector's confidence threshold trade off, and who should decide where it is set?
4. Name two failure modes you observed yourself in Modules 24–25 comparisons.
5. Spaced retrieval: re-answer, cold, two questions of your choice from the Phase 1 and Phase 2 gates. If they have evaporated, schedule a review week before the capstone.
6. Assignments 1–3 genuinely completed — their built-in sanity checks and expected values pass, not merely "the notebook runs."

---

[← Phase 2 — Deep Learning](3-deep-learning.md) · [Curriculum overview](../README.md) · [Next: Phase 4 — Capstone →](5-capstone.md)
