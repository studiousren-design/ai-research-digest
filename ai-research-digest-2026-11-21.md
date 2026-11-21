# AI Research Digest — 2026-11-21

Note: search snippets only; publication dates are inferred from arXiv IDs (2611.xxxxx = November 2026; 2611.25135 is dated 18 Nov 2026). No in-window item was found for AI in education, so only three stories are included, all from priorities 1–2.

**[Prompting / RAG / In-context learning]** — "The Price of Choosing Examples: Context Overfitting in Adaptive In-Context Learning" proves a finite-sample bound on how much adaptively selected examples can overfit. Experiments on Banking77 across 64 retrieval recipes and two model families show a selected context only improves risk when the selection procedure is stable enough for its evidence to transfer.
*For your build:* In Layer 2, treat example-retrieval as something that can overfit: hold out a validation set of queries, compare several retrieval recipes, and prefer stable selection rules over highly query-tuned ones.
Source: https://arxiv.org/abs/2611.21251

**[Prompting / RAG / In-context learning]** — "Revisiting What Makes a Good Context Subset: A Sparse Latent Basis Perspective" frames few-shot demonstration selection as choosing a subset that jointly covers the information a query needs, and introduces residual selection (RES) as a diagnostic. Across seven benchmarks and eight LLMs, it finds top-k similarity retrieval does not always beat zero-shot.
*For your build:* In Layer 2, replace pure top-k similarity with complementary/residual selection (each added example should cover what the earlier ones miss), and test against a zero-shot baseline from Layer 1.
Source: https://arxiv.org/html/2611.19220

**[Alignment / Feedback & critique loops]** — "Calibrated Decision Rewards: Training Language Models with a Judge That Knows How Sure It Is" has the LLM judge output calibrated confidence rather than raw scores, which are overconfident, position-biased and gameable. Using this as the reward ranked correct above incorrect answers more often at every difficulty level, with no sign of reward hacking during training.
*For your build:* In Layer 3, have the critic return a confidence along with its verdict and only trigger revision (or escalate to a human expert) when confidence is high that the answer is wrong or low that it is right.
Source: https://arxiv.org/pdf/2611.25135

**Wider Field** — Omitted: nothing clearly groundbreaking was verifiable within the last 7 days from search snippets.
