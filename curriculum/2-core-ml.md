# Phase 1 — Core ML Foundation (CS229)

**Modules 13–17 · Primary course: Stanford CS229 Machine Learning · Typical duration: 3–5 months**

*If this phase clicks, everything that follows becomes less mysterious.*

## Course links

- Course page: <https://cs229.stanford.edu/>
- Stanford Online: <https://online.stanford.edu/courses/cs229-machine-learning>
- YouTube lectures (Autumn 2018, Andrew Ng) — all lecture numbers below refer to this playlist: <https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU>. A [Spring 2022 offering](https://www.youtube.com/playlist?list=PLoROMvodv4rNyWOpJg_Yh4NSqI4Z4vOYy) (Tengyu Ma & Chris Ré) exists if you prefer newer delivery, but the lecture numbers and problem sets here are keyed to 2018 — classical ML does not rot.
- Course notes (PDF): linked from cs229.stanford.edu — download all and keep them open while watching
- Problem sets (Autumn 2018 materials, mirrored): <https://github.com/maxim5/cs229-2018-autumn> — **the problem sets are required in this phase, not optional.** Lectures teach recognition; problem sets teach recall under pressure. Do at least Problem Sets 1 and 2, checking against the posted solutions only after a real attempt.

## Module 13 — Supervised learning: linear regression and gradient descent

**Topics:**

- Lectures 1–3: Intro, Linear Regression and Gradient Descent, Locally Weighted & Logistic Regression
- CS229 Notes: Part I — Supervised Learning
- Implement linear regression from scratch in NumPy — no scikit-learn yet
- Start Problem Set 1

**Resources:**

- Re-read "A Few Useful Things to Know About Machine Learning" (Domingos, 2012) — you read it in Module 12; it reads differently after Lecture 1: <https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf>

**Math checkpoint:** if the matrix notation in Lecture 2 is unclear, revisit your Imperial College Course 1 (Linear Algebra) notes — specifically the matrix multiplication and dot product sections.

**▸ Build:** NumPy linear regression on the California housing dataset. Implement gradient descent by hand. Plot predictions vs actuals and the loss curve. Sanity check: your converged parameters should closely match scikit-learn's `LinearRegression` (or the normal equation). If they do not, your gradient descent has a bug — find it; that hunt is the module.

## Module 14 — Classification: logistic regression, GLMs, and probabilistic classifiers

**Topics:**

- Lectures 3–5: Logistic Regression, Perceptron & Generalized Linear Models, GDA & Naive Bayes
- CS229 Notes: Part I — Classification and Logistic Regression; Generative Learning Algorithms
- scikit-learn: `LogisticRegression`, `train_test_split`, `confusion_matrix`, `classification_report`
- Finish Problem Set 1

**Supplement (gap Stanford leaves):**

- Kaggle Learn — Intro to Machine Learning (free, ~3 hrs). Fills the practical scikit-learn workflow CS229 skips entirely: <https://www.kaggle.com/learn/intro-to-machine-learning>

**Math checkpoint:** GDA and Naive Bayes are your CS109 work in action — Gaussians, Bayes' theorem, and MLE all at once. If the derivations feel shaky, re-read the inference chapters of the CS109 reader before continuing.

**▸ Build:** Binary classifier on a real dataset (Titanic or credit default). Full scikit-learn pipeline: preprocessing, fit, predict, evaluate. Confusion matrix and classification report included. Problem Set 1 completed and checked against solutions.

**⚠ Budget note:** the problem set alone is a module's worth of hours. This module is two to three modules of work — plan 2–3 calendar weeks and do not read slow progress here as falling behind.

## Module 15 — Regularization, bias-variance, and the cost of complexity

**Topics:**

- Lectures 8–9: Data Splits, Models & Cross-Validation; Approximation/Estimation Error & ERM
- CS229 Notes: Regularization and Model Selection
- Visualize bias-variance: train models of increasing complexity, plot train vs validation error
- Lectures 6–7 (Support Vector Machines, Kernels) — required before Problem Set 2, which uses kernels; not load-bearing for Phase 2 onward

**Supplement:**

- 3Blue1Brown — "Gradient descent, how neural networks learn" (20 min). Good visual reinforcement of what your calculus now means in practice: <https://www.youtube.com/watch?v=IHZwWFHWa-w>

**Math checkpoint:** if the gradient derivations feel hand-wavy, revisit your Imperial College Course 2 notes on the chain rule — you have done this, it will reconnect.

**▸ Build:** Add L1 and L2 regularization to your Module 14 classifier. Compare coefficients and validation performance across at least five lambda values spanning three orders of magnitude. Document findings in a Markdown cell — explain the result so that a colleague who did not run the experiment could follow it.

## Module 16 — Ensemble methods: trees, random forests, gradient boosting

**Topics:**

- Lecture 10: Decision Trees and Ensemble Methods
- scikit-learn: `DecisionTreeClassifier`, `RandomForestClassifier`, `GradientBoostingClassifier`
- Cross-validation properly: `StratifiedKFold`, `GridSearchCV` — not just a single train/test split
- XGBoost quickstart: <https://xgboost.readthedocs.io/> — it will show up in real work
- Start Problem Set 2

**Supplement (gap):**

- Udemy — "Machine Learning A-Z" (Eremenko), tree and ensemble sections only. Better applied walkthrough of ensemble methods than CS229 provides: <https://www.udemy.com/course/machinelearning/>

**▸ Build:** Three-model comparison: logistic regression vs random forest vs gradient boosting, all evaluated with stratified cross-validation. Report each model's score as mean ± standard deviation across folds, and state explicitly whether the gap between the top two models is larger than the fold-to-fold noise — if it is not, your recommendation paragraph must say so. One paragraph explaining which you would recommend and why.

## Module 17 — Unsupervised learning, evaluation, and phase wrap-up

**Topics:**

- Lectures 14–15: Expectation-Maximization Algorithms (includes K-means and mixtures of Gaussians), PCA and ICA — note the playlist has two videos labeled "Lecture 15"; you want "PCA and ICA"
- Apply PCA to your dataset: reduce to 2D and visualize cluster separation
- Refactor one of your Modules 13–16 notebooks into clean, documented, shareable code
- Finish Problem Set 2
- Heading to a real Masters afterward? Do Problem Set 3's EM/GMM derivations too — that is what graduate homework feels like
- Write a phase retrospective in your log: what clicked, what is still fuzzy, what math gaps remain

**⚠ Note:** EM is MLE with hidden variables — your CS109 likelihood work is the key that opens it. And PCA in CS229 will connect directly to your math-phase Course 3 work. This is where that effort pays off.

**▸ Build:** A clean, documented ML pipeline: data loading, preprocessing, model selection, cross-validated evaluation, results table. Done when it runs top-to-bottom on a fresh clone without edits. Problem Set 2 completed and checked against solutions.

**⚠ Budget note:** finishing Problem Set 2 makes this two to three modules of work. Plan for it; the phase duration already does.

## Optional companion for this phase

- StanfordOnline **Statistical Learning with Python** (Hastie & Tibshirani, free to audit) follows the ISLR book and covers the same classical-ML ground more gently. Course and free book at <https://www.statlearning.com/>. Use it if CS229's pace bruises; do not use it to avoid the problem sets.

## Completion gate

Before moving to Phase 2, all five of these must be true:

1. You can explain the bias-variance tradeoff, why we use cross-validation, and what regularization does — without looking anything up.
2. You can explain what maximum likelihood estimation is and name two CS229 algorithms that are MLE underneath.
3. You compare two models with 5-fold CV: A scores 0.84 ± 0.03, B scores 0.85 ± 0.03. Is B better? You can say what you would check or do before claiming it is.
4. Problem Sets 1 and 2 are genuinely attempted and checked — not read.
5. Spaced retrieval: re-answer, cold, two questions of your choice from the math phase gate.

If not, spend one more module here. Phase 2 builds directly on these concepts.

---

[← Phase 0 — Setup](1-setup.md) · [Curriculum overview](../README.md) · [Next: Phase 2 — Deep Learning →](3-deep-learning.md)
