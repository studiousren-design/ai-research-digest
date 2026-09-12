# AI Research Digest — 2026-09-12

---

## One story cleared the bar this week

Eight searches were run across prompting/RAG/in-context learning, alignment/critique loops, and AI-in-education, plus a general sweep for the wider-field pick. Most returns were evergreen surveys, aggregator "weekly AI news" roundups, or arXiv papers whose IDs place them well outside the 5–12 September window despite surfacing in "2026" search summaries. The one AI-education paper that looked most relevant — an ISEDJ piece on human-AI collaboration in knowledge transfer — is already in the covered-stories list from a prior week. Alignment/critique-loop searches surfaced only papers from earlier in 2026 (self-critique RL, meta-rewarding, self-distillation feedback) with no new dated item in this window. Wider-field candidates this week — a reported (unconfirmed) NVIDIA acquisition of Hugging Face, expanded regulator access to frontier models for cyber evaluation, and a UNECE data-center energy forecast — read as business, policy, or infrastructure news rather than a genuine capability jump or paradigm shift, so that section is omitted rather than forced.

**[Prompting / In-Context Learning]** — A new paper, "Data Efficient Sample Selection for In-Context Learning" (arXiv 2609.06670), frames the choice of which few-shot demonstrations to put in a prompt as a subset-ranking problem rather than independent example scoring. Its method, DearICL, uses a differentiable sorting objective inside a gap-index bandit to pick demonstration combinations that generalize to unseen queries, instead of relying on static, task-level example sets.
*For your build:* Layer 2 (RAG examples) — rather than retrieving the top-k most similar examples independently, consider scoring candidate example *sets* for how well they complement each other, which the paper suggests transfers better to queries unlike anything in your example pool.
Source: https://arxiv.org/abs/2609.06670
