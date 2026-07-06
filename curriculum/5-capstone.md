# Phase 4 — Capstone: A Real System

**Modules 26–28 · No new primary course · Typical duration: 2–4 months**

*This is where learning becomes skill and skill becomes credibility.*

You are consolidating and building — the capstone **is** the phase. Choose a problem relevant to a domain you actually work in or care about, even a simplified or prototype version of a real challenge.

## Capstone minimum requirements

- **Data pipeline** — repeatable, documented, versioned — and **at least one messy data source**: something that requires real cleaning, labeling, or deduplication decisions, documented in the README. Clean benchmark datasets teach modeling; messy data teaches engineering.
- **Model training script or notebook** — clean, not a scratch pad
- **Evaluation report** — quantitative metrics against a simple baseline, **with uncertainty on the headline metric** (a bootstrap confidence interval or variance across seeds — a point estimate alone does not support "beats the baseline"), qualitative error analysis, and an **explicit leakage check**: state how you guaranteed no test information reached training (temporal splits, group splits, dedup across splits — whichever applies)
- **Simple demo** — FastAPI endpoint, Gradio app, or Streamlit UI — **containerized** (see Module 26)
- **README** — problem statement, approach, results, how to reproduce, and a **model-card-style limitations section**: what the system was evaluated on, what it has NOT been tested on, and known failure modes (see "Model Cards for Model Reporting", Mitchell et al., 2019: <https://arxiv.org/abs/1810.03993>)
- **Reader-ready write-up** — one page a non-ML engineer could read and act on

## Module 26 — System design, scaffolding, and the production skeleton

**Topics:**

- Define your capstone problem in one sentence. Write it in your README now, before you touch any data.
- Map your data pipeline: source → preprocessing → features → model → output → evaluation
- Set up experiment tracking: [Weights & Biases free tier](https://wandb.ai/) or [MLflow](https://mlflow.org/)
- Identify your evaluation criteria before training anything. What does good look like?
- **Scoped MLOps** — three production basics, kept deliberately small:
  - Write a Dockerfile for your demo and run it in the container
  - Add one GitHub Actions workflow that runs a smoke test (data loads, model loads, one prediction) on push
  - Log every prediction your demo makes (inputs, output, timestamp) to a file — the seed of monitoring
- Pick the matching lessons from [MLOps Zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp) (DataTalks.Club, free) or [Made With ML](https://madewithml.com/) (Goku Mohandas, free) — scoped to Docker/CI/logging only, per the one-spine rule. Do not do either course end-to-end now.

**Resources:**

- Chapters 1–2 of *Designing Machine Learning Systems* by Chip Huyen (O'Reilly). The best framing of what a real ML system requires: <https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/>

**▸ Build:** Documented project plan in your README: problem statement, data sources (including the messy one), evaluation criteria + leakage strategy, and a project board with issues for Modules 27 and 28. Dockerfile and CI workflow committed and green.

**⚠ Note:** Scope down. A narrow, well-executed project with honest evaluation is a stronger signal than an ambitious, half-finished one. The scoping decision itself is an engineering skill.

## Module 27 — Build, evaluate, and iterate

**Topics:**

- Wrangle the messy data source first — document every cleaning decision and why you made it
- Train your baseline model. Log it. Do not optimize before you have a baseline.
- Run your evaluation, including the leakage check. Identify the top 3 failure modes — not just the metric, but what is actually failing and why.
- Iterate on one failure mode. Log the change and the result.
- Get one peer review: walk a friend or colleague through what you built and what broke.
- Draft a 5-minute verbal explanation of your system for a non-technical listener.

**▸ Build:** Trained baseline model with tracked experiments. At minimum two iterations logged. Error analysis and leakage check written in Markdown. A verbal walkthrough you have practiced once.

## Module 28 — Polish, demo, and retrospective

**Topics:**

- Finish the demo: FastAPI, Gradio, or Streamlit, running in its container, logging predictions. Functional over beautiful.
- Write the README: problem, approach, results, limitations (model-card style), next steps for a production version
- Write a technical brief (1 page): what you built, what it can and cannot do, what it would take to ship it — written for a technically literate non-expert reader
- Write your final retrospective in the log: what you would do differently, what surprised you, where your gaps remain
- Share it: post the repo link. LinkedIn, a relevant Slack or Discord, or a blog.

**▸ Build:** A complete, shareable project: containerized working demo with CI, clean repo, published README with limitations section, and a one-page technical brief you could present in an engineering review. Acceptance test: someone who has never seen the repo goes from `git clone` to the running containerized demo using only the README — if that requires you standing behind them, it is not done.

**⚠ Note:** The technical brief is the most important deliverable of the entire curriculum. The ability to communicate a system's capabilities and limits clearly is what makes you credible — to employers, collaborators, and yourself.

---

[← Track A — NLP](4a-nlp.md) / [Track B — Vision](4b-vision.md) · [Curriculum overview](../README.md) · [Next: Beyond the curriculum →](6-beyond.md)
