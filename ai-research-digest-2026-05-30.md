# AI Research Digest — 2026-05-30

---

**[Feedback / Critique Loop]** — OpenAI and Thrive Holdings describe a three-step automated self-improvement loop for a tax-preparation AI built on Codex: the system first captures field-level discrepancies between the model's predicted values and the actual filed returns, then clusters recurring failure patterns to separate noise from actionable defects, and finally auto-generates bounded improvement tasks with explicit success criteria for Codex to address. Over six weeks, this loop lifted filing completion accuracy from 25% to 86% without any manual model retraining, demonstrating that a structured error-taxonomy pipeline can compound domain gains far faster than ad-hoc fine-tuning.

*For your build:* Wire Layer 3 to accumulate failures by error type across a session rather than reacting to each critique individually — only trigger a prompt-refinement task when a pattern crosses a frequency threshold, so each Layer 3 correction targets a verified recurring defect rather than a noise spike.

Source: https://openai.com/news/rss.xml

---

**[Prompting Technique]** — Google's Gemini 3 API introduces a `thinking_level` parameter (0–100 scale) that lets developers tune reasoning depth at inference time without swapping models, and pairs it with `thoughtSignature` tokens that must be echoed back in subsequent turns to preserve the model's accumulated reasoning state. These two primitives formally decouple *how hard the model thinks* from *what reasoning it has already done*, enabling cheap shallow passes for retrieval and deep deliberate synthesis from the same model within a single orchestration loop.

*For your build:* Route calls by layer: low `thinking_level` for Layer 2 retrieval passes (fast, high-throughput) and high `thinking_level` for the Layer 3 critique pass (slow, high-depth), threading the `thoughtSignature` between them so the critic inherits full reasoning context from the retrieval step rather than restarting cold.

Source: https://blog.google/technology/ai/rss/

---

**[AI in Education / Expert Knowledge Transfer]** — Google published results from a pre-registered eight-week randomised controlled trial across 48 math classrooms (≈ 1,800 junior-secondary students) in Sierra Leone, comparing the Guided Learning AI tutor against standard instruction. This is among the first large-scale causal studies of AI tutoring in a low-resource context, and it reports quantified effect sizes on learning gains and teacher workload rather than proxy benchmark scores, providing rare empirical grounding for AI-in-education claims.

*For your build:* The RCT finding that structured scaffolding outperforms open-ended AI assistance in learning contexts directly informs Layer 2 design — pre-specify retrieval examples with explicit framing (learner level, known misconception, target concept) rather than leaving context selection unconstrained, because structured example framing reliably outperforms letting the model choose its own context.

Source: https://blog.google/technology/ai/rss/

---

**Wider Field**

**[Gemini 3.5 Flash outperforms Gemini 3.1 Pro at coding]** — Google released Gemini 3.5 Flash at I/O 2026 and it surpasses the prior-generation Pro model on agentic coding and Terminal-Bench benchmarks (76.2% vs 70.3%), while retaining Flash-tier speed and cost. A Flash model decisively beating its contemporary Pro on reasoning-intensive tasks challenges the assumption that capability scales monotonically with model size and generation.

*Why it might matter later:* If smaller-but-newer models consistently exceed larger-but-older models on reasoning tasks, the compute-optimal retrieval strategy for Layer 2 may shift from "use the biggest model for synthesis" toward "use the freshest model for synthesis," making recency of model weights a first-class architecture signal alongside capability ranking.

Source: https://blog.google/technology/ai/rss/
