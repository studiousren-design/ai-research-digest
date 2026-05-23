# AI Research Digest — 2026-05-23

---

**[LLM Alignment]** — Jack Clark's Import AI 457 (May 18) spotlights a new safety paradigm called *positive alignment*: rather than enumerating prohibited behaviors, it orients AI systems toward fundamentally cooperative dispositions that are argued to generalize better to novel situations where no specific prohibition yet exists. Unlike negative-rule alignment that fails at gaps in its enumeration, a positive disposition toward cooperation is hypothesised to hold even when the model encounters edge cases outside its training distribution.

*For your build:* Rewrite the Layer 1 system prompt around affirmative cooperative goals ("this assistant genuinely helps researchers by…") rather than a list of prohibitions — the Layer 3 critique loop can then evaluate responses against that positive orientation and flag divergence, rather than searching exhaustively for violated rules that may not exist for novel query types.

Source: https://jack-clark.net/feed/

---

**[AI in Education / Expert Knowledge Transfer]** — Google launched Gemini for Science at I/O 2026 (May 19), anchored by Co-Scientist: a multi-agent system modelled on the scientific method that runs an "idea tournament" in which agents continuously generate, debate, and rank research hypotheses until the strongest survive. Alongside it, Science Skills integrates over 30 life-science databases — UniProt, AlphaFold, AlphaGenome, InterPro — into a callable skill bundle, collapsing complex bioinformatics workflows from hours to minutes; the Co-Scientist research papers are published in *Nature*.

*For your build:* The idea-tournament pattern is a ready-made Layer 3 blueprint — spawn two or three critique agents with deliberately different evaluation criteria on the same retrieved example set, let them score each other's selections, and surface only the candidates that survive the debate into Layer 1 context, rather than relying on a single-pass critique.

Source: https://blog.google/technology/ai/rss/

---

**[Prompting / In-Context Architecture]** — Google's new Interactions API, released in public beta at I/O 2026 (May 19), introduces a typed, native representation for agentic conversations: interleaved messages, model reasoning traces ("thoughts"), tool calls, and session state are first-class objects in the context rather than flattened text strings. This structured context model replaces ad-hoc prompt concatenation and makes reasoning traces inspectable and attributable at the object level.

*For your build:* Adopting typed context objects in Layer 2 means retrieved RAG examples carry provenance metadata (source, retrieval score, chunk type) that Layer 3 can critique independently of content — the critique loop can then penalise low-confidence retrievals before they pollute Layer 1, without having to parse provenance from raw text.

Source: https://blog.google/technology/ai/rss/

---

**Wider Field**

**[AI produces first original proof resolving a named open conjecture]** — An OpenAI model disproved the 80-year-old Erdős unit-distance conjecture, constructing a valid proof that exploits an unexpected bridge between algebraic number theory and discrete geometry; the proof was subsequently verified and refined by human collaborators. This is the first reported instance of an AI system independently originating a result that closes a named open problem in mathematics, not merely solving a competition problem with a known answer.

*Why it might matter later:* If AI can discover structural connections across distant mathematical domains without being directed to look there, the same exploratory search could eventually be applied to retrieval — surfacing cross-domain analogies in Layer 2 that a purely semantic similarity index would never surface on its own.

Source: https://openai.com/news/rss.xml
