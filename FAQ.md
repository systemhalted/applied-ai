# Frequently Asked Questions

## Is this equivalent to a Masters degree?

No, and it does not pretend to be. Measured plainly, completing this curriculum is comparable to seriously auditing 3–4 graduate courses with substantial projects — roughly 250–300 hours of budgeted work (realistically 400–600 invested) versus ~1,500+ hours for a 30-credit MS, with one specialization instead of several electives and no exams or graded feedback beyond the courses' own problem sets. What it does give you: a from-the-math-up foundation, a portfolio of working systems, and preparation that makes a real Masters' ML, deep learning, and specialization coursework feel comfortable — though the proof-based algorithms core and proctored exams most programs require are [a separate muscle this curriculum does not train](curriculum/6-beyond.md#when-to-do-a-real-masters-instead). If you need the credential itself, see [When to do a real Masters instead](curriculum/6-beyond.md#when-to-do-a-real-masters-instead).

## Can I skip the math phase?

If you can pass the [completion gate](curriculum/0-mathematics.md#completion-gate--do-not-start-phase-0-until-you-can-answer-all-nine) cold — all nine questions, written answers, no peeking — yes, skip ahead. If you can *almost* pass it, do the modules covering the gaps. If you are tempted to skip because the math feels slow, do not: CS229 without linear algebra, calculus, and probability is a lecture series you watch instead of a skill you build. Partial math is worse than no math — it creates confident confusion.

## Coursera costs money. Do I have to pay?

Mostly no. Coursera courses can be **audited free** (video content, no graded assignments) — look for the small "Audit" link during enrollment. The catch: this curriculum requires doing the Imperial College graded assignments, which auditing excludes. Options: pay for the months you actually use (via subscription, typically ~$49–59/month or Coursera Plus, region-dependent — finish in 3 months, pay for 3), apply for [Coursera financial aid](https://learner.coursera.help/hc/en-us/articles/209819033-Apply-for-financial-aid-or-a-scholarship) (real, but takes ~2 weeks per course), or substitute the assignments with the exercises in the free [MML book](https://mml-book.github.io/). One optimization: Modules 7–9 (CS109) are entirely free — pause the subscription during those months. Everything else load-bearing in the curriculum — Stanford lectures, CS109, problem sets, HuggingFace courses — is genuinely free.

## I can't stream video — is there a text path?

Yes, the whole way through. The CS109 course reader and the MML book cover the math phase (Modules 1–11) in full. The CS229 lecture notes — which the curriculum already tells you to download and keep open — carry Phase 1. The famously complete [cs231n.github.io notes](https://cs231n.github.io/) carry Track B, and CS224N's lecture notes carry Track A. And when you can watch, the Stanford, 3Blue1Brown, and Karpathy YouTube lectures all have captions.

## What will compute cost me?

Between $0 and roughly $50 total. Everything through Phase 1 runs on a laptop CPU. From Phase 2's CNN work onward you want a GPU: Google Colab's free tier and Kaggle's weekly GPU quota cover the whole curriculum if you tolerate session limits. A month or two of Colab Pro (~$10/month) during the specialization track buys convenience, not capability. One real extra: Track A's final two modules need an LLM behind an API — about $5–10 of API credit, or a small open model you serve yourself. Details in [the compute guidance](curriculum/1-setup.md#compute-guidance--decide-this-now-not-mid-phase).

## How do I choose between the NLP and vision tracks?

Choose **Track A (NLP/LLMs)** unless you specifically work with visual data. LLM skills currently compound faster for most applied AI work, and Track B's most modern content (CLIP, VLMs) increasingly overlaps with language models anyway. The full decision guide is at the end of [Phase 2](curriculum/3-deep-learning.md#choose-your-specialization-track--before-module-21-and-commit). Whichever you pick: one track, completely. The other can be an elective after the capstone.

## How long will this actually take?

At a sustainable 5–6 hours per week: about two years. A module is ~5–6 focused hours of work, and most people with a job and a life complete one every 1–4 calendar weeks. If that number disappoints you, read the pacing note in the [README](README.md#how-to-use-this-curriculum) — the consistency is the point. Full-time learners can compress the calendar dramatically, but do not compress the sequence.

## I fell behind / missed a month. Do I restart?

No. Resume from exactly where you are. Do not double up to catch up — that is how people quit. The sequence matters; the calendar does not.

## How do I get help when I'm stuck?

1. **The completion gates and math checkpoints** in each phase point you to the specific resource for your gap — use them first.
2. **GitHub Discussions** on this repo — ask there; someone else is stuck on the same thing.
3. **Course-specific communities:** the fast.ai forums, the HuggingFace Discord, and r/learnmachinelearning are active and beginner-tolerant.
4. **Find a cohort:** 2–3 people starting the same month, a weekly 30-minute check-in. This is the single strongest predictor of finishing. Post in Discussions to find each other.

## Can I use ChatGPT/Claude/Copilot while doing the builds?

Use AI to *explain* things without limit — it is a superb tutor. For the builds, type the from-scratch implementations yourself (NumPy regression, backprop, MLE, PCA): the entire point of those exercises is what your hands learn. For everything downstream of the fundamentals — debugging, plotting, scaffolding — use whatever makes you faster. The test is simple: could you pass the phase's completion gate without the assistant open?

## Why isn't [popular course/book] included?

Probably because of the one-spine rule: one primary course per phase, supplements only where a real gap exists. More resources make a curriculum weaker, not stronger — choice is where self-learners go to die. If you believe a resource genuinely *replaces* something here (better, freer, more current), see [CONTRIBUTING.md](CONTRIBUTING.md).

## The curriculum says "domain" a lot. What if I don't have one?

Pick the data type closest to what you already know: your industry, a hobby with data, a dataset you are genuinely curious about. The domain's job is to make the builds feel real instead of academic. Tabular business data is the safest default; it is everywhere and every employer has it.
