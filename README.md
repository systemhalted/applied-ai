# Applied AI — an open curriculum

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)
![Modules](https://img.shields.io/badge/modules-28-orange.svg)

> From solid programming skills to hands-on AI engineering — one course spine, a working build in every module, and honest pacing for people with jobs and lives.

Applied AI is a free, self-paced curriculum for going from solid programming skills to credible, hands-on AI engineering. It follows a single spine of world-class courses — **Imperial College mathematics + Stanford CS109 → Stanford CS229 → CS230 → CS224N or CS231n → a capstone system** — and requires you to build something real at every step. One cost caveat: the required Imperial College graded assignments sit behind Coursera's subscription; the [FAQ](FAQ.md) covers audit limits, financial aid, and a free substitute.

It is inspired by the [OSSU](https://github.com/ossu) curricula, but narrower and more opinionated: one primary course per phase, a build deliverable on every module card, required problem sets, and paid resources only where the free spine leaves a real practical gap.

## Who this is for

Anyone who:

- can already program comfortably (Python strongly preferred), and
- wants working, from-scratch understanding of machine learning — not just API familiarity, and
- can commit **5–6 focused hours per week**, sustainably, for the long haul.

No prior ML or advanced math background is assumed — the curriculum starts by building the math. If Python itself is new to you, complete a free intro first — [Python for Everybody](https://www.py4e.com/) or the [University of Helsinki Python MOOC](https://programming-25.mooc.fi/) — this curriculum does not teach programming.

## What this is — and is not

**This is** a serious foundation: honestly measured, it is comparable to deeply auditing 3–4 graduate courses with real problem sets and a substantial portfolio project — roughly 250–300 hours of budgeted module work, and realistically 400–600 hours of total invested time over about two years once stuck-time, review, and the messy weeks are counted.

**This is not** a Masters degree, and it does not claim to be. A 30-credit MS is ~1,500+ hours with several electives, exams, and graded feedback. What this curriculum optimizes for is the *practitioner* outcome: you can build, evaluate, and explain real ML systems, and prove it with artifacts. If you need the credential, this curriculum is excellent preparation — see [When to do a real Masters instead](curriculum/6-beyond.md#when-to-do-a-real-masters-instead).

## What you will be able to do

- **Understand ML from the math up** — you implement linear regression, backpropagation, maximum likelihood estimation, and PCA in raw NumPy before using the framework version of each.
- **Build working systems every module** — a concrete deliverable on every card, from a gradient-descent implementation to a LoRA fine-tune (cheaply adapting a large language model) or a zero-shot CLIP comparison (classifying images with no training at all).
- **Do the real coursework** — CS229 problem sets and the Stanford assignments are required gate items, not suggestions.
- **Specialize** in NLP/LLMs or computer vision through a full Stanford graduate course, ending at the current frontier (agents and evals, or multimodal models).
- **Finish with a portfolio capstone** — a containerized, CI-tested ML system with rigorous evaluation, a model-card-style limitations section, and a one-page technical brief.
- **Explain what you build** — every phase includes plain-English writing exercises, because communicating a system's capabilities and limits is half the job.

## Curriculum

A **module** is a unit of work — roughly 5–6 focused hours — not a calendar week. Working alongside a job, most people finish a module in 1–4 calendar weeks. Modules that carry a required problem set or Stanford assignment are two to three modules' worth of hours — their cards say so, and the phase durations already account for it. At that pace the full curriculum takes **about two years**. That is by design: a consistent 5 hours per week over months compounds into something real; three intense weekends do not.

| Phase | Primary course | Modules | Typical duration |
|---|---|---|---|
| [Pre — Mathematics](curriculum/0-mathematics.md) | Imperial College Mathematics for ML + Stanford CS109 | 1–11 | 5–10 months |
| [0 — Setup & Domain Selection](curriculum/1-setup.md) | — | 12 | 1–2 weeks |
| [1 — Core ML Foundation](curriculum/2-core-ml.md) | Stanford CS229 (+ required problem sets) | 13–17 | 3–5 months |
| [2 — Deep Learning Fundamentals](curriculum/3-deep-learning.md) | Stanford CS230 | 18–20 | 2–4 months |
| [3 — Specialization: Track A (NLP/LLMs)](curriculum/4a-nlp.md) *or* [Track B (Vision)](curriculum/4b-vision.md) | Stanford CS224N *or* CS231n (+ required assignments) | 21–25 | 4–6 months |
| [4 — Capstone: A Real System](curriculum/5-capstone.md) | — | 26–28 | 2–4 months |
| [Beyond the curriculum](curriculum/6-beyond.md) | RL elective, more electives, papers, staying current | — | ongoing |

Track your progress with the [PROGRESS.md checklist](PROGRESS.md).

**Choosing a specialization track:** pick **Track A (NLP/LLMs)** unless you specifically work with visual data — LLM skills compound faster for most applied AI work today. Full guidance is at the end of [Phase 2](curriculum/3-deep-learning.md#choose-your-specialization-track--before-module-21-and-commit). One track, completely; the other can be an elective later.

## How to use this curriculum

**Day one — five steps, in order:**

1. Read [Who this is for](#who-this-is-for) and [What this is — and is not](#what-this-is--and-is-not) above. Decide.
2. If you already know some of the math, take the [Phase Pre completion gate](curriculum/0-mathematics.md#completion-gate--do-not-start-phase-0-until-you-can-answer-all-nine) as a placement test — written answers, no peeking — and skip the modules whose questions you pass cold.
3. Create your companion repo (`ai-learning-lab` with `notebooks/ | projects/ | weekly-log/ | data/`) and copy [PROGRESS.md](PROGRESS.md) into it.
4. Read the [Coursera cost answer in the FAQ](FAQ.md#coursera-costs-money-do-i-have-to-pay) and decide: pay monthly, apply for financial aid, or take the free MML-substitute path — before you enroll.
5. Open [Module 1](curriculum/0-mathematics.md) and start.

**One spine, not a playlist.** Each phase has exactly one primary course. Supplements exist only where the spine leaves a practical gap, and they are always scoped ("tree and ensemble sections only"). Resist the urge to add more resources — finishing one course well beats sampling five.

**The weekly rhythm — four things, every week:**

1. **Watch / Read** (60–90 min) — 2–3 lectures or assigned readings
2. **Code** (45–60 min) — a small exercise, problem-set work, or extension of the module's build
3. **Build** (60–90 min) — the deliverable listed on each module card
4. **Log** (15 min) — one entry in your learning log: what clicked, what broke, what changed

The four items sum to under five hours; the rhythm plus the inevitable stuck-time is your 5–6.

**What "Build" means:**

- Not a production system. A working notebook or script with clean output you could show a colleague.
- Reproducibility over sophistication. A well-documented baseline beats a hacked SOTA clone.
- If a module gets messy: do the Build, skip the Log. Never skip both.

**Keep a companion repository** (day-one step 3). The log inside it is not optional — it is the mechanism that turns passive consumption into engineering memory. Treat it like a decision log, not a diary.

**Respect the gates.** Every phase from the math onward ends with a completion gate — questions you must answer *in writing* before moving on, plus required problem sets in the course phases. After writing your answers, check them: against the course notes, a study partner, or an AI tutor asked to find the flaw in each answer. Self-graded and confidently wrong is the failure mode to defend against. The math gate includes a calibration example of what a passing answer looks like — that depth is the bar for every gate in this curriculum.

**A note on pacing:**

- Some weeks will be messy. That is expected and not a failure.
- If you miss a week: resume from where you are. Do not try to catch up by doubling the next one.
- The sequence matters more than the timing. Stretch phase durations as your schedule requires.
- The goal is not to finish the plan. The goal is to become the kind of engineer who can evaluate, build, and explain AI systems — and to have built enough to prove it.

## Getting help

Read the [FAQ](FAQ.md) first — it covers costs, pacing, skipping, and where to ask questions. This repo's GitHub Discussions tab is the place to find study partners and ask curriculum questions; course-specific help lives in the fast.ai forums, the HuggingFace Discord, and r/learnmachinelearning. The single strongest predictor of finishing is a cohort of 2–3 people on the same schedule — find one.

## Contributing

Found a broken link, an error, or a clearly better free resource? See [CONTRIBUTING.md](CONTRIBUTING.md) and use the matching issue template. Note that the curriculum is deliberately minimal — replacements are welcome, additions rarely are. All participation is governed by the [Code of Conduct](CODE_OF_CONDUCT.md).

## License

[MIT](LICENSE)
