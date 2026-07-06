# Phase Pre — Mathematics for Machine Learning

**Modules 1–11 · Primary courses: Imperial College Mathematics for ML (Coursera) + Stanford CS109 · Typical duration: 5–10 months**

*Complete this before Phase 0. It is the foundation everything else is built on.*

This phase has two spines, taken in order. The Imperial College Mathematics for Machine Learning Specialization on Coursera covers linear algebra and calculus (with a PCA course as its finale). Stanford CS109 covers probability and statistics — which Imperial College deliberately omits, and which CS229 depends on from its second week (maximum likelihood, Gaussians, Naive Bayes, EM). The goal here is to finish both well, not just finish them.

Already comfortable with some of this? The [completion gate at the bottom](#completion-gate--do-not-start-phase-0-until-you-can-answer-all-nine) doubles as a placement test — skip the modules whose questions you can answer cold (from memory, nothing open), in writing.

## Course links

- Imperial College specialization page: <https://www.coursera.org/specializations/mathematics-machine-learning>
- Course 1 — Linear Algebra: <https://www.coursera.org/learn/linear-algebra-machine-learning>
- Course 2 — Multivariate Calculus: <https://www.coursera.org/learn/multivariate-calculus-machine-learning>
- Course 3 — PCA: <https://www.coursera.org/learn/pca-machine-learning>
- Stanford CS109 — Probability for Computer Scientists: lectures (2022, Chris Piech): <https://www.youtube.com/playlist?list=PLoROMvodv4rOpr_A7B9SriE_iZmkanvUg> · free course reader: <https://chrispiech.github.io/probabilityForComputerScientists/en/> · course site: <https://web.stanford.edu/class/cs109/>
- Companion reference (free PDF): *Mathematics for Machine Learning* — Deisenroth, Faisal, Ong — <https://mml-book.github.io/>

**A note on cost:** the Imperial graded assignments require a Coursera subscription (auditing excludes them). Financial aid exists, and the MML book's exercises are an accepted free substitute — decide before enrolling; the [FAQ covers all three paths](../FAQ.md#coursera-costs-money-do-i-have-to-pay). CS109 (Modules 7–9) is entirely free.

## Modules 1–3 — Linear Algebra (Imperial College Course 1)

**Topics:**

- Vectors and vector spaces — the language of all ML data representations
- Matrix multiplication, inverses, and transformations — how models apply weights
- Dot products, projections, and orthogonality — the geometry behind similarity
- Eigenvalues and eigenvectors — critical for PCA, covariance, and understanding gradients

**Resources:**

- Imperial College Course 1, all weeks — do all graded assignments; do not continue in free audit mode without them. The exercises are where the concepts land.

**Supplement:**

- 3Blue1Brown Linear Algebra playlist — watch the relevant chapter *after* each course lecture, not before: <https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab>

**▸ Build:** All Course 1 assignments completed. A learning-log entry listing the three concepts that felt least solid and why. These are your watch points for the Core ML phase.

**⚠ Note:** Eigenvalues and eigenvectors feel abstract here. They will click when you hit PCA in Modules 10–11, and again in CS229 ([Module 17](2-core-ml.md#module-17--unsupervised-learning-evaluation-and-phase-wrap-up)). Note them, do not chase them.

## Modules 4–6 — Multivariate Calculus (Imperial College Course 2)

**Topics:**

- Derivatives and the chain rule — the mechanical heart of backpropagation
- Partial derivatives and gradients — what gradient descent is actually computing
- The Jacobian and Hessian — how CS229 talks about optimization formally
- Taylor series approximations — used throughout CS229 loss function derivations

**Resources:**

- Imperial College Course 2, all weeks, with graded assignments

**Supplement:**

- 3Blue1Brown Calculus playlist, Chapters 1–8, for visual intuition alongside the course: <https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr>

**▸ Build:** All Course 2 assignments completed. Implement the chain rule by hand for a 3-step composite function in Python — not using autograd. Write out each derivative step in a notebook comment. Verify each hand-computed derivative against a finite-difference approximation — (f(x+h) − f(x−h)) / 2h with small h. Agreement to several decimal places is your proof it is right; disagreement means find the error before moving on.

**⚠ Note:** The chain rule exercise is more important than it sounds. In [Module 18](3-deep-learning.md#module-18--neural-network-basics-forward-pass-loss-backpropagation) you will implement backpropagation in NumPy. Learners who skipped this step find it mysterious. Learners who did it find it mechanical.

## Modules 7–9 — Probability and Statistics (Stanford CS109)

**Topics:**

- Counting and combinatorics — the mechanics under discrete probability
- Conditional probability, independence, and Bayes' theorem — the grammar of inference
- Random variables, expectation, and variance — how uncertainty is quantified
- Common distributions: Bernoulli, binomial, Poisson, uniform, normal — and when each shows up
- Joint distributions and the Central Limit Theorem — why the normal distribution is everywhere
- Maximum likelihood and MAP estimation — the statistical engine inside most of CS229
- Bootstrapping, confidence intervals, and hypothesis testing — how to tell whether model A is *actually* better than model B, which you will need in every evaluation you ever run

**Resources:**

- CS109 2022 lectures, from Counting through Maximum Likelihood Estimation, plus the bootstrapping and hypothesis-testing lectures — work the corresponding parts of the free course reader alongside; its problems are the graded work here
- Course reader: <https://chrispiech.github.io/probabilityForComputerScientists/en/>

**Supplements:**

- *Mathematics for Machine Learning*, Chapter 6 (Probability and Distributions) — <https://mml-book.github.io/>
- 3Blue1Brown — "Bayes theorem, the geometry of changing beliefs": <https://www.youtube.com/watch?v=HZGCoVF3YvM>
- StatQuest Statistics Fundamentals playlist for any topic that will not click: <https://www.youtube.com/playlist?list=PLblh5JKOoLUK0FLuzwntyYI10UQFUhsY9>

**▸ Build:** A probability notebook in three parts: (1) simulate coin flips and dice to verify the law of large numbers and the CLT empirically; (2) implement Bayes' theorem on a concrete medical-test example and confirm it by simulation; (3) implement maximum likelihood estimation for a Gaussian's mean and variance in NumPy from scratch, and bootstrap a confidence interval for your estimates — your MLE results should equal the sample mean and (biased) sample variance; confirm they do. Plus a plain-English paragraph explaining Bayes' theorem to someone who has never studied probability.

**⚠ Note:** This is the section most self-taught curricula skip, and it is why CS229 loses people in its second week. MLE is not an optional detail — linear regression, logistic regression, GDA, Naive Bayes, and EM are all maximum likelihood in different costumes. Arrive knowing what a likelihood is.

## Modules 10–11 — Dimensionality Reduction with PCA (Imperial College Course 3)

**Topics:**

- Covariance matrices and variance — what data spread looks like in matrix form (your CS109 variance work, now in matrix clothing)
- PCA as an eigenvalue problem — connects Course 1 directly to a real ML algorithm
- Projection and reconstruction — the geometry of compression
- Apply PCA in Python using NumPy — implement it from scratch, not just scikit-learn

**Resources:**

- Imperial College Course 3, all weeks, with graded assignments

**Supplement:**

- StatQuest — "Principal Component Analysis (PCA), Step-by-Step" (YouTube, 22 min) — excellent visual complement: <https://www.youtube.com/watch?v=FgakZw6K1QQ>

**▸ Build:** PCA implemented from scratch in NumPy on a real dataset. Visualize the top 2 principal components. Confirm correctness: your components should match scikit-learn's PCA up to sign, and your explained-variance ratios should match closely. Write a plain-English explanation of what PCA is doing — one paragraph, no equations.

**⚠ Note:** The plain-English explanation is not a throwaway. Being able to explain PCA to someone without an ML background in one paragraph is exactly the kind of communication skill this curriculum trains alongside the technical work. Course 3 is also harder than it looks — give it the full two modules.

## What to do alongside this phase

- Start your companion repository now: `ai-learning-lab` with folders `notebooks/ | projects/ | weekly-log/ | data/`
- The Builds from Module 4 onward need Python, Jupyter, and NumPy. If you do not have a working setup, do the environment checklist in [Phase 0](1-setup.md) now — Module 12's remaining work (domain choice, compute plan) still waits until after the math.
- Keep a running `WEEKLY_LOG.md` through the math phase. It is good practice and creates continuity into Phase 0.
- Do not start CS229 until the math is complete. Partial math is worse than no math — it creates confident confusion.

## Completion gate — do not start Phase 0 until you can answer all nine

1. What does it mean to multiply two matrices? What does the result represent geometrically?
2. What is an eigenvalue and what does it tell you about a transformation?
3. What is a partial derivative and how does it differ from an ordinary derivative?
4. What is the chain rule and why does it matter for training neural networks?
5. State Bayes' theorem and explain what each term means with a concrete example.
6. What is the difference between the expectation and the variance of a random variable?
7. Name three common probability distributions and a situation where each naturally appears.
8. What does maximum likelihood estimation do, in one sentence, and why does ML care?
9. What does PCA do, and why might you use it before training a model?

If any of these produce a blank, spend one more module on the relevant course section before moving on.

**Calibration** — a passing answer to Q8 looks like: *"MLE picks the parameter values under which the observed data would have been most probable; ML cares because linear regression, logistic regression, and Naive Bayes are all maximum likelihood under different modeling assumptions."* One crisp paragraph at that depth, per question, is the bar. A one-line definition is not a pass.

---

[← Curriculum overview](../README.md) · [Next: Phase 0 — Setup →](1-setup.md)
