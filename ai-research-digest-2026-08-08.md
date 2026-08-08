# AI Research Digest — 2026-08-08

---

**[LLM Alignment — Critique Loops]** — A new verifier-free test-time framework, "Refining Over Resampling" (Bilal et al., posted 6 August 2026), has LLMs iteratively self-critique and refine each of several independent reasoning rollouts rather than just sampling more of them, then aggregates the refined answers by majority vote. Across AIME24/25, AMC, OlympiadBench, and MATH500, this refine-then-vote approach beats greedy decoding, plain majority voting, verifier-based best-of-N, beam search, and lookahead decoding on open-weight models.
*For your build:* For Layer 3 (critique loop), this suggests refining each candidate output in place — having the critique agent revise a draft rather than only accept/reject it — before aggregating across parallel attempts; most useful specifically when you lack a ground-truth verifier to score candidates against.
Source: https://arxiv.org/abs/2608.05643

---

## Prompting/RAG and AI-education: nothing cleared the bar this week

Searches for fresh prompting/RAG/in-context-learning advances and for AI-in-education/expert-knowledge-transfer research (arXiv listings, lab blogs, and news roundups) turned up only: evergreen surveys with no dated primary source in the 1–8 August window; papers with arXiv IDs placing them months earlier despite surfacing in "2026" search summaries (e.g. several May/June 2026 tutoring-prompt-optimization and RAG-agent-memory papers); and older studies outside the 7-day cutoff (a Google DeepMind classroom trial reported 2 July, a Coursera higher-ed report from February). An Allen Institute (Ai2) August newsletter item on replacing RAG retrieval with semantic-embedding key-value memory for agents looked promising, but its underlying paper and exact publish date couldn't be independently verified (the newsletter page was unreachable this session), so it's excluded rather than published on an unconfirmed source. No item in either category met both the recency and verification bar, so neither slot is filled this week rather than forcing a weak match.

## Wider Field

**[OpenAI's Astra solves 10 decades-old open math problems]** — On 1 August 2026, OpenAI published a 249-page manuscript in which an internal version of its upcoming "Astra" model family produced solutions — with machine-checked Lean 4 proof certificates — to ten previously unsolved problems in mathematics and theoretical computer science, several untouched by mathematicians for over a decade. The compute run behind the results reportedly cost around $2,000.
*Why it might matter later:* If machine-checkable AI-generated proofs for genuinely open problems become routine, the bottleneck in mathematical research could shift from "can a proof be generated" to "which open problems are worth pointing a model at" — changing who sets research agendas and how mathematical claims get trusted.
Source: https://www.forbes.com/sites/jonmarkman/2026/08/03/openais-astra-solved-10-decades-old-math-problems-for-just-2000/
