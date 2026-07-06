# Beyond the Curriculum

The core curriculum makes you a credible practitioner. This appendix covers what comes after: elective courses, a paper-reading sequence, habits for staying current, where supplements fill real gaps along the way — and a word about actual degrees.

## Recommended first elective: Reinforcement Learning

RL is the one core ML paradigm the curriculum's spine never touches, and it keeps resurfacing (RLHF trained the models you used in Track A; OMSCS's core ML course is roughly one-third RL, so this elective is doubly recommended if you are Masters-bound). Take it as your first post-capstone elective, with a build:

- **Primary:** the free [HuggingFace Deep RL Course](https://huggingface.co/learn/deep-rl-course) (hands-on, modern tooling) — or David Silver's classic UCL/DeepMind lectures for stronger theory: <https://davidsilver.uk/teaching/>
- **Depth:** OpenAI's *Spinning Up in Deep RL* — the best bridge from RL concepts to working code: <https://spinningup.openai.com/>
- **▸ Build:** train an agent on a Gymnasium environment (CartPole then LunarLander), plot learning curves across three hyperparameter settings, and write the usual one-paragraph plain-English explanation of what the reward signal is doing.

## Stanford electives — where they fit

These courses are not part of the core curriculum. They are the right next steps depending on what your work demands. Take them after the capstone, not alongside it.

| Course | Take it when | Skip it if |
|---|---|---|
| [CS221 — AI Principles](https://cs221.stanford.edu/) | After CS229, if you need search, planning, or MDP foundations | Your goal is purely applied ML systems — you can return to it |
| [CS234 — Reinforcement Learning](https://web.stanford.edu/class/cs234/) | As the rigorous follow-up to the RL elective above | The HuggingFace course + Spinning Up covered what your work needs |
| [CS224U — Natural Language Understanding](https://web.stanford.edu/class/cs224u/) | After CS224N, if semantics and reasoning depth matter for your NLP work | CS224N already gave you what you need for most LLM application work |
| [CS336 — Language Modeling from Scratch](https://stanford-cs336.github.io/) | After Track A, if you want to build the full LM pipeline — tokenizer, training, inference — with your own hands | You consume LLMs rather than build them; Track A Module 25 already covered the applied layer |
| [CS229M — Machine Learning Theory](https://web.stanford.edu/class/stats214/) | A "depth semester" after 12+ months of practice, if you want to read theory papers fluently | Your goal is shipping systems — proofs slow you down before practice is solid |
| [CS228 — Probabilistic Graphical Models](https://ermongroup.github.io/cs228-notes/) (free notes) | You are heading to a theory-forward MS — CMU MSML lists PGMs as core | Your goal is applied systems; modern deep learning routes around most of it |
| [Convex Optimization — Boyd & Vandenberghe](https://web.stanford.edu/~boyd/cvxbook/) (free book) | Same as above — it is the other CMU MSML core this curriculum never touches | Your goal is applied systems; autograd has already done this for you |

Also worth a scoped look after Track A: tool schemas are increasingly standardized as MCP servers — the free [HuggingFace MCP Course](https://huggingface.co/learn/mcp-course/unit0/introduction) is the follow-up to Module 25's agent work if your projects go further in that direction.

Lecture playlists:

- CS221: <https://www.youtube.com/playlist?list=PLoROMvodv4rOca_Ovz1DvdtWuz8BfSWL2>
- CS234: <https://online.stanford.edu/courses/cs234-reinforcement-learning>
- CS224U: <https://www.youtube.com/playlist?list=PLoROMvodv4rPt5D0zs3YhbWSZA8Q_DyiJ>
- CS229M: <https://www.youtube.com/playlist?list=PLoROMvodv4rP8nAmISxFINlGKSK4rbLKh>

## When to do a real Masters instead

This curriculum is serious, but it is not a degree — see [What this is — and is not](../README.md#what-this-is--and-is-not). If you need the credential (visa, promotion committee, research ambitions, career switch where HR filters on degrees), the right move is a real program, and the value benchmark is [Georgia Tech's OMSCS](https://omscs.gatech.edu/): a fully online, accredited MS in CS with an ML specialization for under ~$10k total. This curriculum prepares you well for its ML coursework — and covers most of the same applied ground if the credential is not what you need.

Know what a real program will demand that this curriculum does not build. OMSCS's ML specialization requires a graduate **algorithms** core course — dynamic programming, graph algorithms, NP-completeness, proof-based homework, proctored exams — and nothing here trains that muscle. Before enrolling, work through a proof-based algorithms resource: [MIT 6.006 on OCW](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-spring-2020/) or Jeff Erickson's free [*Algorithms*](https://jeffe.cs.illinois.edu/teaching/algorithms/) book. Expect timed, proctored exams in most graduate courses; this curriculum's written gates are practice for the understanding, not the format. And on admissions: your capstone and companion repo are hiring evidence, but OMSCS admission runs on prior coursework and recommendations, and competitive programs (CMU MSML and peers) weigh GPA and research — do not plan on a portfolio substituting for either.

## Supplements — where they fill real gaps

Stanford is strong on theory and architecture. It is lighter on practical tooling, API workflows, and applied pipelines. These resources — most free, a few paid — are integrated at the specific modules where that gap appears; none are required.

| Resource | Platform | Used in | Gap it fills |
|---|---|---|---|
| Kaggle Learn — Intro to ML | Kaggle (free) | [Module 14](2-core-ml.md#module-14--classification-logistic-regression-glms-and-probabilistic-classifiers) | scikit-learn practical workflow that CS229 skips |
| Machine Learning A-Z, tree & ensemble sections (Eremenko) | Udemy | [Module 16](2-core-ml.md#module-16--ensemble-methods-trees-random-forests-gradient-boosting) | Applied ensemble methods walkthrough |
| Statistical Learning with Python (Hastie & Tibshirani) | StanfordOnline / free book | [Modules 13–17](2-core-ml.md) (optional) | Gentler classical-ML companion to CS229, follows ISLR |
| deeplearning.ai Deep Learning Specialization | Coursera | [Modules 18–20](3-deep-learning.md) (optional) | Graded assignments alongside CS230 for structured practice |
| fast.ai Practical Deep Learning, Lessons 1–2 | fast.ai (free) | [Module 20](3-deep-learning.md#module-20--cnns-and-the-structure-of-deep-learning-projects), [Track B Module 22](4b-vision.md#module-22--transfer-learning-and-modern-architectures) | Top-down CNN and transfer learning workflow |
| Transformers for NLP (Lazy Programmer) | Udemy | [Track A Module 23](4a-nlp.md#module-23--fine-tuning-transfer-learning-with-transformers) | Fine-tuning workflow detail CS224N leaves to you |
| PyTorch for Deep Learning (Daniel Bourke) | Udemy | [Track B Module 23](4b-vision.md#module-23--object-detection-and-segmentation) | Applied detection pipeline CS231n leaves abstract |
| MLOps Zoomcamp / Made With ML | free | [Module 26](5-capstone.md#module-26--system-design-scaffolding-and-the-production-skeleton) | Docker, CI, and prediction logging for the capstone |
| Designing Machine Learning Systems (Chip Huyen) | O'Reilly / book | [Module 26](5-capstone.md#module-26--system-design-scaffolding-and-the-production-skeleton) | Production system thinking |

## Paper reading sequence — 1 paper per 2 weeks, after the capstone

1. [Attention Is All You Need](https://arxiv.org/abs/1706.03762) (Vaswani et al., 2017)
2. [BERT: Pre-training of Deep Bidirectional Transformers](https://arxiv.org/abs/1810.04805) (Devlin et al., 2018)
3. [Language Models are Few-Shot Learners (GPT-3)](https://arxiv.org/abs/2005.14165) (Brown et al., 2020)
4. [Training Compute-Optimal Large Language Models (Chinchilla)](https://arxiv.org/abs/2203.15556) (Hoffmann et al., 2022) — why model size stopped being the whole story
5. [Training Language Models to Follow Instructions (InstructGPT)](https://arxiv.org/abs/2203.02155) (Ouyang et al., 2022)
6. [Direct Preference Optimization](https://arxiv.org/abs/2305.18290) (Rafailov et al., 2023) — the simplification that replaced much of the RLHF pipeline
7. [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685) (Hu et al., 2021)
8. [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073) (Anthropic, 2022)
9. [FlashAttention: Fast and Memory-Efficient Exact Attention](https://arxiv.org/abs/2205.14135) (Dao et al., 2022)
10. [DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning](https://arxiv.org/abs/2501.12948) (DeepSeek, 2025) — the openly documented recipe behind reasoning models
11. [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03993) (Mitchell et al., 2019) and [Datasheets for Datasets](https://arxiv.org/abs/1803.09010) (Gebru et al., 2018) — short, and they will change how you document everything

For the ethics and responsibility dimension the papers only gesture at, fast.ai's free [Practical Data Ethics](https://ethics.fast.ai/) course is the standout structured resource.

## Practices that compound after the curriculum

- **Evaluate before you deploy.** Define the evaluation suite before building the model. This is the discipline that separates engineering from prototyping.
- **Version prompts like code.** A prompt library with review history is a production artifact.
- **Keep a decision log.** What model, when it was trained, what it was evaluated against, why it was chosen. Future-you will need it.
- **Teach what you learn.** Present a paper or demo to peers monthly — a study group, a meetup, your team. Explaining is the fastest way to find your own gaps.
- **Practice the one-page technical brief** from the capstone on every project — it is the most reusable communication tool this curriculum develops.
- **Build a vocabulary for uncertainty.** Learn to say "this model is accurate on X but has not been tested on Y" with confidence.

## Staying current — 30 minutes per week

- [The Batch](https://www.deeplearning.ai/the-batch/) (deeplearning.ai) — weekly digest, practical and low-hype
- [Import AI](https://importai.substack.com/) (Jack Clark) — deeper, more research-oriented
- [Hugging Face Papers](https://huggingface.co/papers) — trending papers with linked code and models (the successor niche to the retired Papers With Code); favor what is reproducible, not just published
- [Andrej Karpathy on YouTube](https://www.youtube.com/@AndrejKarpathy) — the clearest thinker on LLM internals working publicly

---

[← Phase 4 — Capstone](5-capstone.md) · [Curriculum overview](../README.md)
