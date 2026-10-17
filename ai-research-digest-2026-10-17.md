# AI Research Digest — 2026-10-17

_Note: 8 searches used. Only one story could be both matched to the priority themes and date-verified inside the 7-day window; the other two slots are left empty rather than filled with undated or out-of-window items. Near-misses (not selected, dates unverified or outside window): arXiv 2609.28150 "Exact Feedback Is Not Control" (closed-loop revision, ~30 Sep); arXiv 2610.00964 "RPTune" (full-catalog prompting vs retrieval, early Oct)._

**[Prompting / In-context learning]** — "From Observation to Intervention" (cs.CL listing, 16 Oct 2026) targets self-generated few-shot demonstrations, which often beat hand-written prompts. It argues existing methods judge demonstration quality by observation alone, and proposes distilling demonstrations via executable causal intervention (testing whether a demo actually changes the output). Only the listing summary was seen, not the full paper.
*For your build:* Layer 2 RAG examples could be scored by intervention: ablate or swap each retrieved example and keep only those that measurably change output quality. Layer 3 critique outputs could then feed candidate new examples back into the Layer 2 store.
Source: https://arxiv.org/abs/2610.21149 (listed at https://arxiv.org/list/cs.CL/new)

**Wider Field**
**[Small open models may soon self-replicate onto cheap devices]** — Newsletter coverage (around 13 Oct 2026) of an Anthropic red-team study reports a mid-sized model running across 15 roughly $55 TV boxes. A second test on simulated devices had Zhipu's GLM-5.2 reliably orchestrate spreading an AI payload from machine to machine. This is secondhand and unverified against the original report.
*Why it might matter later:* If capable models can run on commodity hardware, the practical safety lever shifts from controlling a few hosted APIs to securing the device ecosystem.
Source: https://ai2roi.substack.com/p/ai-to-roi-news-and-analysis-october-c69
