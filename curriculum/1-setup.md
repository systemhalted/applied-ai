# Phase 0 — Setup & Domain Selection

**Module 12 · No new course · Typical duration: 1–2 weeks**

*Eliminate all friction before CS229 starts. One module, no new concepts.*

You have finished the math phase and passed the completion gate. This module is purely mechanical. No new concepts. The goal is to have everything installed, structured, and working so that when the Core ML phase starts you open your laptop and start — not troubleshoot.

## Module 12 — Environment, tooling, and domain selection

**Topics:**

- Verify your environment: Python 3.11+, Jupyter Lab, PyTorch, scikit-learn, NumPy, pandas, matplotlib
- If not installed: use [Anaconda](https://www.anaconda.com/) or pyenv + pip for clean version management
- Confirm your companion repo structure: `ai-learning-lab` with `notebooks/ | projects/ | weekly-log/ | data/`
- Run `hello_pytorch.ipynb`: create a tensor, multiply two matrices, run a linear layer forward pass
- Choose your project domain: text/NLP, tabular business data, or computer vision
- Decide your compute plan (see below)

**Resources:**

- "A Few Useful Things to Know About Machine Learning" (Domingos, 2012) — 10 pages, free PDF: <https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf>. Read it now, before CS229, so the first lecture has context.

**▸ Build:** `hello_pytorch.ipynb` runs clean and is committed to your companion repo. Domain choice and compute plan are written in its README. A one-paragraph note in your log on why you chose that domain.

**⚠ Note:** Domain choice shapes every build project in the phases ahead. Pick a domain close to work you actually do or data you genuinely care about — not the one that sounds most impressive.

## Compute guidance — decide this now, not mid-phase

Everything through Phase 1 runs fine on a laptop CPU. From [Module 20](3-deep-learning.md#module-20--cnns-and-the-structure-of-deep-learning-projects) (CNN on CIFAR-10) onward, and for all fine-tuning work in the specialization tracks, you want a GPU. Self-learners stall here more than anywhere else, so pick a plan up front:

- **[Google Colab](https://colab.research.google.com/)** (free tier) — enough for CIFAR-10 CNNs and DistilBERT-scale fine-tuning, with session limits and occasional GPU unavailability. The default choice.
- **[Kaggle Notebooks](https://www.kaggle.com/code)** — a generous weekly GPU quota (around 30 hours) and persistent datasets; a solid free alternative when Colab throttles you.
- **Paid, ~$10–50/month** — Colab Pro or [Lightning AI Studios](https://lightning.ai/) buy longer sessions and better GPUs. A month or two during the specialization track is plenty; unnecessary before then.
- **Own NVIDIA GPU** — if you have one with 8 GB+ VRAM, local is simplest; everything in this curriculum fits.
- Nothing here is Colab-specific: any Jupyter environment with a GPU — local, university, or a regional cloud notebook service — fills the same role if Colab or Kaggle is unreachable where you are.
- **Track A only:** Modules 24–25 (RAG evaluation, agents) additionally need an LLM behind an API. Budget roughly $5–10 of API credit with any major provider, or plan to serve a small open model locally or on Colab. If no major provider operates in your country, or you have no international payment card, the locally served open model is a full substitute, not a degraded one — local servers expose the same API shape. Decide which now so it is not a surprise 18 months in.

## Math reference map — use reactively throughout CS229 and CS230

- Linear algebra questions: your Imperial College Course 1 notes + 3Blue1Brown Linear Algebra playlist (Chapters 1–9): <https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab>
- Calculus questions: your Imperial College Course 2 notes + 3Blue1Brown Calculus playlist (Chapters 1–8): <https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr>
- Probability and statistics questions: the CS109 course reader (<https://chrispiech.github.io/probabilityForComputerScientists/en/>) + StatQuest — [Statistics Fundamentals playlist](https://www.youtube.com/playlist?list=PLblh5JKOoLUK0FLuzwntyYI10UQFUhsY9) (free)
- Full reference textbook (free): *Mathematics for Machine Learning* — <https://mml-book.github.io/>

---

[← Phase Pre — Mathematics](0-mathematics.md) · [Curriculum overview](../README.md) · [Next: Phase 1 — Core ML →](2-core-ml.md)
