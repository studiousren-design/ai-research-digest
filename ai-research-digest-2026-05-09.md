# AI Research Digest — 2026-05-09

---

**[Multimodal RAG]** — Google upgraded Gemini API File Search to natively process images and text together using the Gemini Embedding 2 model, adding custom metadata filtering and page-level citations so retrieval results are fully auditable. Developers can now build RAG pipelines that ground answers in visual evidence—charts, annotated slides, diagrams—alongside text, with citations pointing to the exact page or image used.
*For your build:* Layer 2 (RAG examples) can now index over visual research content and retrieve both text and image evidence in a single pass; the page-level citations give your Layer 3 critique loop a concrete anchor to verify factual grounding rather than relying on semantic plausibility alone.
Source: https://blog.google/innovation-and-ai/technology/developers-tools/expanded-gemini-api-file-search-multimodal-rag/

---

**[Async Critique Agent]** — OpenAI shipped Auto-review for Codex: a dedicated reviewer agent that sits at the sandbox boundary and evaluates boundary-crossing actions in milliseconds rather than blocking for synchronous human sign-off. Evaluated on internal Codex trajectories, it achieves 99.93% effective action approval while blocking 99.3% of prompt injection attacks and reducing mandatory human interventions by roughly 200×.
*For your build:* Layer 3 (critique loop) can adopt this async-reviewer pattern—running a fast specialist critic in parallel with the main generation step rather than as a serial blocking pass, keeping end-to-end latency low while still catching misaligned or high-risk outputs before they reach the user.
Source: https://alignment.openai.com/auto-review

---

**[Agentic Alignment Critic]** — Google's 2026 Responsible AI Progress Report (published May 6) introduces a "User Alignment Critic"—a dedicated sub-agent that vetoes actions by other agents whenever they deviate from user intent—as part of a multi-layer agentic safety framework that also includes Agent Origin Sets for data-access restriction and automated red-teaming pipelines. The report also updates Google's Frontier Safety Framework with Critical Capability Levels (CCLs), adding a new CCL for systematic harmful manipulation.
*For your build:* The User Alignment Critic is a direct blueprint for decomposing Layer 3: split your critique pass into a fast intent-alignment check (does this action serve the user's stated goal?) and a slower safety sweep, mirroring how Google separates these two concerns rather than conflating them in one monolithic critic.
Source: https://blog.google/innovation-and-ai/products/responsible-ai-2026-report-ongoing-work/

---

## Wider Field

**[AI Systems Automating AI Research]** — Jack Clark's Import AI 455 (May 4) synthesises a milestone in the automation of AI R&D: Claude Mythos Preview now achieves a 52× mean speedup on LLM optimisation tasks versus a skilled human researcher (up from 30× with Opus 4.6 in February), CORE-Bench—a benchmark for reproducing scientific results—was effectively solved at 95.5% accuracy, and AI systems can now post-train models to reach roughly half the performance gains that human researchers achieve manually. Taken together, these data points suggest AI has crossed into reliably automating multi-hour expert research tasks end to end.
*Why it might matter later:* If this trajectory continues, the feedback loop in which AI accelerates its own research could compress years of safety and alignment work into months—meaning the window to establish robust oversight before AI researchers outpace human reviewers may be shorter than current roadmaps assume.
Source: https://jack-clark.net/2026/05/04/import-ai-455-automating-ai-research/
