# AI Research Digest — 2026-10-31

**Prompting / In-Context Learning** — A cross-domain evaluation compares zero-shot, few-shot, retrieval-augmented and automatic prompt-optimisation approaches across tasks. Few-shot prompting peaked at 77.83% average accuracy with 200 demonstrations, but scaling behaviour was inconsistent across tasks.
*For your build:* Don't assume more Layer 2 examples is monotonically better: cap the number of retrieved examples and test the curve per task type, since returns are uneven and extra examples may add noise.
Source: https://arxiv.org/html/2610.24913

**Prompting / In-Context Learning** — "Multi-Target Few-Shot Prompting with Diffusion Language Models" uses a demonstrated edit (e.g. an API migration) to guide infilling of multiple masked regions at once, rather than one left-to-right generation per site.
*For your build:* When Layer 2 examples demonstrate a transformation (e.g. weak answer → expert answer), structure them as input/edit pairs so the same pattern can be applied consistently across several parts of a response.
Source: https://arxiv.org/abs/2610.22294

**LLM Alignment / Critique Loops** — Rubricon generates and refines evaluation/training rubrics without human preference labels, using observed criterion pass rates on sample model responses together with LLM self-critique. Its rubrics align 9% more closely with expert-authored rubrics than the best alternative synthetic method tested.
*For your build:* Use Layer 3's critique rubric as a living artefact: score sample outputs against each criterion, drop criteria that never discriminate, and rewrite those that do not match expert judgement.
Source: https://arxiv.org/abs/2610.38220

Notes: Dates were inferred from arXiv 2610.* identifiers (October 2026); snippets did not give exact submission dates. No qualifying education/expert-knowledge story within 7 days was found (the closest, arXiv 2608.07488, is from August). No Wider Field item is included: the week's candidates (e.g. open-weight and cyber-model releases) came only from secondary roundups and did not clearly qualify as paradigm shifts.
