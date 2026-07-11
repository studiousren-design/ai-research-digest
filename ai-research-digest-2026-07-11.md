# AI Research Digest — 11 July 2026

---

**[RAG / Long-Context Retrieval]** — A new paper, "Hierarchical Sparse Attention Done Right: Toward Infinite Context Modeling," proposes a hierarchical sparse-attention mechanism intended to cut the quadratic cost of standard attention while preserving the ability to attend across very long inputs. The goal is effectively unbounded context windows, which bears directly on how much retrieved evidence a RAG pipeline can pass to a model in a single call.
*For your build:* Layer 2 (RAG examples) — if this scales as described, you could feed substantially more retrieved passages per query without aggressive pre-truncation, shifting the design burden from chunk-ranking toward context budgeting.
Source: https://arxiv.org/abs/2607.02980

---

**[LLM Alignment / Critique Loop]** — "LLM-as-a-Verifier: A General-Purpose Verification Framework" proposes using an LLM as a domain-agnostic verifier that checks another model's output for correctness, rather than relying on bespoke, task-specific verifiers built separately for each domain. It's designed to plug into arbitrary generation pipelines as a standalone checking stage.
*For your build:* Layer 3 (critique loop) — replacing your task-specific critique prompt with a general-purpose verifier role could let one reusable component validate outputs across multiple task types instead of maintaining separate critique prompts per task.
Source: https://arxiv.org/abs/2607.05391

---

**[Expert Knowledge Transfer / Auditing]** — "Physics-Audited Agentic Discovery in Scientific Machine Learning" describes an agentic AI system for scientific discovery whose candidate findings are checked against known physical laws and constraints before being accepted, instead of being trusted on pattern-matched output alone. This grounds an agent's autonomous exploration in domain-expert knowledge rather than statistical plausibility.
*For your build:* Layers 2/3 — encoding hard domain constraints as an explicit audit step (rather than only as soft RAG examples) could catch outputs that are fluent but violate known facts, complementing retrieval rather than replacing it.
Source: https://arxiv.org/abs/2607.07379

---

## Wider Field

**[Recursive self-improvement: from bounded self-refinement to autonomous research loops]** — A new survey, "Recursive Self-Improvement in AI: From Bounded Self-Refinement to Autonomous Research Loops," maps the progression of self-improvement techniques from simple bounded self-refinement (a model critiquing and revising a single output) toward fully autonomous research loops, where systems iteratively improve themselves with progressively less human oversight. The paper frames this as one of the fastest-growing subfields of AI research in 2026.
*Why it might matter later:* If autonomous research loops mature past bounded self-refinement, the bottleneck on AI progress shifts from designing critique steps to auditing and constraining those loops — making verification work, like the physics-audited discovery system above, increasingly load-bearing rather than optional.
Source: https://arxiv.org/abs/2607.07663
