# AI Research Digest — 2026-11-14

Note: only 1 of the 3 requested stories could be verified as published within the last 7 days (since 2026-11-07) using the 8-search budget. Candidates found for other categories were dated 2026-11-03 (RAGCompass 2611.05596, SME-C critique/refinement 2611.05749) and were excluded as outside the window; education searches returned nothing in-window. No Wider Field item clearly qualified, so that section is omitted.

**[RAG / In-context learning]** — A study of six LLMs on 81 CodeContests problems compares zero-shot, random-retrieval and similarity-based retrieval prompting for algorithmic problem-solving. Similarity-based RAG gave consistent net gains (about 20.4% pass rate vs 17.9% zero-shot and 17.3% random retrieval), suggesting example relevance matters more than simply adding examples.
*For your build:* Layer 2 should rank retrieved examples by similarity to the current task rather than sampling them, and it is worth running a random-retrieval control to confirm the retrieval step adds value beyond extra context; Layer 1 can stay fixed while Layer 2 varies.
Source: https://arxiv.org/html/2611.09791
