# Contributing

Thank you for wanting to improve Applied AI! Contributions of all kinds are welcome.

## What makes a good contribution

- **Fixing broken or moved links.** Courses get rehosted and playlists disappear. If you find a dead link, a pull request with the updated URL (or the best current equivalent) is always welcome.
- **Correcting errors.** Typos, wrong lecture numbers, misattributed papers, factual mistakes.
- **Improving clarity.** If a module's instructions confused you and you can word them better, propose the change.
- **Suggesting replacement resources.** If a course or video is no longer available, or a clearly better free alternative exists, open an issue explaining what it replaces and why it is better.

## What this curriculum is not looking for

- **More resources.** The curriculum is deliberately one spine, not a playlist. Adding a second course alongside an existing one, or a fifth supplementary video, works against the design. Propose replacements, not additions.
- **Scope expansion.** New phases, new tracks, or new topic areas change what the curriculum is. Open an issue for discussion first — do not start with a pull request.
- **Personal progress content.** Learners keep progress logs in their own companion repositories, not here.

## How to contribute

1. For small fixes (links, typos): open a pull request directly.
2. For anything that changes what a learner does (resources, module content, sequencing): open an issue first and describe the problem the change solves.
3. Keep the module card format intact: Topics → Resources → Supplement → Build → Note.
4. Check links locally before pushing, mirroring CI: `lychee --accept 200,201,204,301,302,303,308,403,429 --timeout 30 "**/*.md"`

## Style

- Match the existing tone: direct, concrete, no hype.
- Every resource entry needs a working link.
- Build deliverables must stay specific and checkable — "understand X" is not a deliverable; "implement X and plot Y" is.

## Maintenance: what the link-check CI cannot see

The weekly lychee run catches dead URLs, but a playlist that was emptied, a course offering that renumbered its lectures or assignments, or a tool that restructured its CLI all still return 200. These pins need an eyeball once a year:

- CS224N assignment numbering (pinned to Winter 2026) and CS231n lecture numbers (pinned to the 2025 offering)
- The CS229 Autumn 2018 playlist and its pset mirror repo
- The three Udemy supplement links (Udemy 403s bots, so CI never sees their real state)
- Tool-facing instructions (lm-evaluation-harness, Ragas) — the curriculum deliberately pins no CLI commands; keep it that way
- The hardcoded module-count badge in the README (currently 28) — it has changed once already

