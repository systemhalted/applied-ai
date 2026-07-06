# Phase 3, Track A — NLP and Large Language Models (CS224N)

**Modules 21–25 · Primary course: Stanford CS224N NLP with Deep Learning · Typical duration: 4–6 months**

*One track. Completely. If you chose [Track B — Computer Vision](4b-vision.md), skip this file.*

## Course links

- Course page: <https://web.stanford.edu/class/cs224n/>
- YouTube lectures: <https://www.youtube.com/playlist?list=PLoROMvodv4rOaMFbaqxPDoLWjDaRAdP9D>
- Stanford Online: <https://online.stanford.edu/courses/cs224n-natural-language-processing-deep-learning>
- Assignments: from the course page. **Required** (numbering per the Winter 2026 offering — assignment and lecture numbers both shift between years, so match by topic): A1 (word vectors), A3 (self-attention and transformers), and A4 (LLM benchmarking and evaluation). A2 (tensor derivatives, dependency parsing) is optional but excellent derivation practice. The assignment notebooks ship with built-in sanity checks and expected outputs — those, not a notebook that merely runs, are the correctness standard.

## Module 21 — Word vectors and language representation

**Topics:**

- CS224N Lectures 1–2: Word2Vec, GloVe, word vector evaluation
- CS224N Assignment A1: word vectors (required)
- Train Word2Vec on a small corpus from your chosen domain using gensim (if gensim fights your environment, train in plain PyTorch or use pretrained vectors — the deliverable is the embedding analysis, not the library)
- Visualize embeddings with t-SNE: nearest neighbors for 10 query words (t-SNE is just a visualization tool here — use scikit-learn's implementation and do not go down the rabbit hole of how it works)

**Resources:**

- "Efficient Estimation of Word Representations in Vector Space" (Mikolov et al., 2013) — the Word2Vec paper, 12 pages: <https://arxiv.org/abs/1301.3781>

**▸ Build:** A notebook that trains embeddings on domain text, visualizes nearest neighbors, and includes a written interpretation: what does the embedding space tell you about your domain? A1 completed.

**⚠ Budget note:** the assignment makes this two to three modules of work — plan 2–3 calendar weeks. Same for every assignment-bearing module in this track.

## Module 22 — Attention, transformers, and the architecture behind LLMs

**Topics:**

- CS224N Lectures 7–9: Attention Mechanism, Transformers, Pre-training
- CS224N Assignment A3: self-attention and transformers (required)
- HuggingFace Transformers: load BERT, run inference, inspect attention weights

**Resources:**

- Andrej Karpathy — "Let's build GPT from scratch" (YouTube, 2 hrs) — essential, not optional: <https://www.youtube.com/watch?v=kCc8FmEb1nY>
- "Attention Is All You Need" (Vaswani et al., 2017) — focus on the architecture diagram and multi-head attention section first: <https://arxiv.org/abs/1706.03762>

**▸ Build:** HuggingFace pipeline: load BERT, run on 50 real examples from your domain, print predictions and confidence scores. Visualize the attention map for at least one example and use it to ground a Markdown explanation of what attention is doing — written for a technically literate colleague who has never touched ML. A3 completed.

## Module 23 — Fine-tuning: transfer learning with transformers

**Topics:**

- CS224N Lectures 10–11: Fine-tuning, NLP downstream tasks
- HuggingFace Trainer API — fine-tune DistilBERT on a text classification task
- HuggingFace Datasets — pick a dataset from your domain area
- Evaluation: F1, precision, recall, and confusion matrix for NLP — not just accuracy

**Supplement (gap):**

- Udemy — "Data Science: Transformers for Natural Language Processing" (Lazy Programmer), fine-tuning section. Fills the practical workflow detail that CS224N leaves to you: <https://www.udemy.com/course/data-science-transformers-nlp/>

**▸ Build:** Fine-tuned DistilBERT classifier that beats a bag-of-words + logistic regression baseline on macro-F1, same train/test split. Clean notebook. A one-page write-up: what you fine-tuned, what data, what metrics, and what you would do next if this were a production system.

**⚠ Note:** Use DistilBERT, not BERT-large. Faster iteration matters more than SOTA performance at this stage. The production write-up is the more important deliverable. If your domain text is not English, use a multilingual checkpoint — `distilbert-base-multilingual-cased` or an XLM-RoBERTa variant, and a multilingual sentence-transformers model for Module 24's RAG embeddings — the workflow is identical.

## Module 24 — LLMs in practice: prompting, RAG, and systematic evaluation

**Topics:**

- CS224N lectures on LLMs, instruction tuning, and RLHF (current offering)
- CS224N Assignment A4: LLM benchmarking and evaluation (required) — this assignment is exactly the skill the industry is short on
- HuggingFace LLM Course, Chapter 7: Main NLP Tasks — free: <https://huggingface.co/learn/llm-course/chapter7/1>
- Build a minimal RAG pipeline: sentence-transformers for embeddings, ChromaDB as vector store, retrieval + generation
- Evaluate the RAG system with [Ragas](https://docs.ragas.io/) — faithfulness, answer relevance, context precision — alongside your own manual judgment. Ragas uses an LLM as its judge and defaults to a hosted provider; if you are on the open-model path, configure it to use your locally served model. Automated metrics and human reading disagree in instructive ways; document where.

**Resources:**

- "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks" (Lewis et al., 2020) — the RAG paper: <https://arxiv.org/abs/2005.11401>

**▸ Build:** A RAG system over 10–20 documents from your domain (use public analogues if needed). Ask it 5 representative questions. Evaluate with Ragas AND manually; write up where the two disagreed. The failure analysis is the deliverable, not the system. A4 completed.

## Module 25 — Fine-tuning at the frontier: LoRA, evals, and agents

The LLM landscape moves fast; this module teaches the three durable practical skills of the current era — parameter-efficient fine-tuning, systematic evaluation, and tool-using agents.

**Topics:**

- Parameter-efficient fine-tuning: LoRA with [HuggingFace PEFT](https://huggingface.co/docs/peft) — fine-tune a small open model (1–3B) on your domain task from Module 23; compare against the full DistilBERT fine-tune on quality, VRAM, and training time
- Read: "LoRA: Low-Rank Adaptation of Large Language Models" (Hu et al., 2021): <https://arxiv.org/abs/2106.09685>
- Systematic evaluation: run your fine-tuned model through [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) on 2–3 relevant benchmarks; understand what the numbers do and do not tell you
- Agents and tool use: the free [HuggingFace Agents Course](https://huggingface.co/learn/agents-course), scoped to the core units on the agent loop, function calling, and structured outputs — skip the framework-specific units for now

**Supplement (depth, optional):**

- Stanford **CS336 — Language Modeling from Scratch** (public lectures): the full pipeline from tokenizer to trained LM. Overkill for this module; the right next course if this track becomes your specialty: <https://stanford-cs336.github.io/>

**▸ Build:** A tool-using agent over your Module 24 RAG system: the agent decides when to retrieve, calls the retriever as a tool, and produces structured output. Run it on 10 tasks; write a failure analysis — where did the agent loop, hallucinate a tool call, or retrieve when it should not have? Plus the LoRA-vs-full-fine-tune comparison table, including the lm-evaluation-harness scores for both models and one sentence on what those benchmark numbers do not tell you about your domain task.

**⚠ Note:** Resist the framework buffet. One agent, built on primitives you understand (a model API plus your own tool schema), teaches more than wiring together three orchestration libraries. And budget for it: this module stacks three skills and is realistically two to three modules of hours — the phase duration accounts for it.

## Completion gate — written, not felt

Answer in your log before starting the capstone:

1. Explain multi-head attention without notes — what problem does it solve that a single attention head does not?
2. When do you fine-tune vs use RAG vs just prompt better? Give a concrete example of each being the right call.
3. What does LoRA freeze and what does it train, and why does that save memory?
4. Name two failure modes of automated LLM evaluation you observed yourself in Modules 24–25.
5. Spaced retrieval: re-answer, cold, two questions of your choice from the Phase 1 and Phase 2 gates. If they have evaporated, schedule a review week before the capstone.
6. A1, A3, and A4 genuinely completed — their built-in sanity checks and expected outputs pass, not merely "the notebook runs."

---

[← Phase 2 — Deep Learning](3-deep-learning.md) · [Curriculum overview](../README.md) · [Next: Phase 4 — Capstone →](5-capstone.md)
