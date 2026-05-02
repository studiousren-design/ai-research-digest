# AI Research Digest — 2026-05-02

> Filtered from: jack-clark.net, thegradient.pub, blog.google, openai.com, bair.berkeley.edu  
> Priority: (1) prompting / RAG / in-context learning, (2) alignment / feedback / critique loops, (3) AI in education / expert knowledge transfer

---

**[RAG & Autonomous Agents]** — Google launched Deep Research Max (April 21, 2026), a next-generation autonomous research agent built on Gemini 3.1 Pro that adds Model Context Protocol (MCP) support and extended test-time compute so the agent can iteratively reason, search, and synthesise across long-horizon tasks. Two tiers ship together: a low-latency variant designed for interactive surfaces and a max-comprehensiveness variant for async background workflows, both generating native inline charts and structured reports directly inside the output.

*For your build:* The MCP integration pattern shows that retrieval should be structured as explicit, composable, version-controlled tool-calls rather than implicit lookups — use MCP-style query-plan sequences as few-shot examples in **Layer 2 (RAG examples)** to teach the model to externalise and self-audit its retrieval strategy before synthesising an answer.

Source: https://blog.google/technology/ai/rss/

---

**[Alignment & Critique Loop]** — OpenAI published a framework for evaluating chain-of-thought (CoT) monitorability across 13 evaluations and 24 environments, finding that frontier reasoning models are generally auditable from outside — and that models that reason for longer are *more* monitorable, not less (April 23, 2026). The full evaluation suite, datasets, and g-mean² metric code were open-sourced so other labs can benchmark their own models' reasoning transparency.

*For your build:* The finding that extended reasoning enhances auditability directly shapes **Layer 3 (critique loop)**: structuring the critique to reason verbosely through each evaluation dimension before issuing a final score makes its judgments more trustworthy and diagnosable; the open-sourced eval suite can be adapted to verify that your critique layer's chain-of-thought predictions are internally consistent with its ratings.

Source: https://openai.com/news/rss.xml

---

**[Expert Knowledge Transfer to AI]** — Anthropic's Automated Alignment Researcher (AAR) project, covered in Import AI 454 (April 20, 2026), showed that Claude models can autonomously design, run, and analyse alignment experiments end-to-end. The best AAR method achieved 0.94 performance on math tasks and 0.47 on coding tasks — roughly double the human baseline — with the key bottleneck being evaluation design (what to measure) rather than experiment execution, suggesting "automated research on outcome-gradable problems is already practical."

*For your build:* The AAR bottleneck maps directly onto **Layer 1 (system prompt)**: the most impactful thing to encode is not *what to do* but *what success looks like* — explicit, outcome-gradable evaluation criteria. AARs succeed when problems are metric-defined, so making Layer 1 metric-explicit (expected output structure, quality dimensions, pass/fail thresholds) directly unlocks automated critique in Layer 3 without needing further human calibration.

Source: https://jack-clark.net/feed/

---

## Wider Field

**[Agentic Orchestration at Scale]** — OpenAI released Symphony (April 27, 2026), an open-source specification for orchestrating coding agents in which every open task on a project board gets a continuously-running agent while humans serve as reviewers rather than authors; early adopters reported 500% increases in landed pull requests. The reference implementation is intentionally minimal — a Markdown workflow policy kept in-repo — so any coding agent can implement its own version in any language.

*Why it might matter later:* If 500% throughput gains reproduce at scale, the critical bottleneck in software development will shift from code generation to code review capacity, which could trigger a re-architecture of engineering teams around AI-native asynchronous merge workflows — effectively repricing human judgment at the review stage rather than the writing stage.

Source: https://openai.com/news/rss.xml
